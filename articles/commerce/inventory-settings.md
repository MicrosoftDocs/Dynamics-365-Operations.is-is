---
title: Nota birgðastillingar
description: Í efnisatriði er fjallað um birgðastillingar og útskýrt hvernig á að nota þær í Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 06/01/2020
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
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 737e71dc73750bf151629fd904081924ac15b91e
ms.sourcegitcommit: 4a981ee4be6d7e6c0e55541535d386bce2565cba
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 07/27/2020
ms.locfileid: "3621222"
---
# <a name="apply-inventory-settings"></a><span data-ttu-id="bf365-103">Nota birgðastillingar</span><span class="sxs-lookup"><span data-stu-id="bf365-103">Apply inventory settings</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="bf365-104">Í efnisatriði er fjallað um birgðastillingar og útskýrt hvernig á að nota þær í Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="bf365-104">This topic covers inventory settings and describes how to apply them in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="bf365-105">Yfirlit</span><span class="sxs-lookup"><span data-stu-id="bf365-105">Overview</span></span>

<span data-ttu-id="bf365-106">Birgðastillingar tilgreina hvort athuga eigi birgða áður en afurðir eru settar í körfuna.</span><span class="sxs-lookup"><span data-stu-id="bf365-106">Inventory settings specify whether inventory should be checked before products are added to the cart.</span></span> <span data-ttu-id="bf365-107">Þær skilgreina einnig birgðatengd skilaboð um smásöluvörur, t.d. „Á lager“ og „Lítið eftir“.</span><span class="sxs-lookup"><span data-stu-id="bf365-107">They also define inventory-related merchandising messages, such as "In stock" and "Only a few left."</span></span> <span data-ttu-id="bf365-108">Þessar stillingar ganga úr skugga um að ekki sé hægt að kaupa afurð ef hún er ekki til á lager.</span><span class="sxs-lookup"><span data-stu-id="bf365-108">These settings ensure that a product can't be purchased if it's out of stock.</span></span>

<span data-ttu-id="bf365-109">Dynamics 365 Commerce leggur mat á lagerstöðu fyrir afurðir.</span><span class="sxs-lookup"><span data-stu-id="bf365-109">Dynamics 365 Commerce provides estimates of on-hand availability for products.</span></span> <span data-ttu-id="bf365-110">Upplýsingar um hvernig áætlað framboð á lager er reiknað er að finna í [Reikna tiltækar birgðir fyrir smásölurásir](calculated-inventory-retail-channels.md).</span><span class="sxs-lookup"><span data-stu-id="bf365-110">For information about how estimated on-hand availability is calculated, see [Calculate inventory availability for retail channels](calculated-inventory-retail-channels.md).</span></span>

<span data-ttu-id="bf365-111">Í Commerce-vefssmið er hægt að skilgreina birgðaþröskuld og birgðabil fyrir afurð eða flokk.</span><span class="sxs-lookup"><span data-stu-id="bf365-111">In Commerce site builder, inventory thresholds and ranges can be defined for a product or a category.</span></span> <span data-ttu-id="bf365-112">Það ákvarðar hvort birgðir geti verið flokkaðar sem á lager, lítið til á lager eða ekki til á lager.</span><span class="sxs-lookup"><span data-stu-id="bf365-112">They determine whether inventory can be classified as in stock, low stock, or out of stock.</span></span> <span data-ttu-id="bf365-113">Frekari upplýsingar er að finna í [Stilla birgðabiðminni og birgðastöðu](inventory-buffers-levels.md).</span><span class="sxs-lookup"><span data-stu-id="bf365-113">For details, see [Configure inventory buffers and inventory levels](inventory-buffers-levels.md).</span></span>

## <a name="inventory-settings"></a><span data-ttu-id="bf365-114">Birgðastillingar</span><span class="sxs-lookup"><span data-stu-id="bf365-114">Inventory settings</span></span>

<span data-ttu-id="bf365-115">Í Commerce eru birgðastillingar skilgreindar í **Stillingar svæðis \> Viðbætur \> Birgðastjórnun** í svæðissmið.</span><span class="sxs-lookup"><span data-stu-id="bf365-115">In Commerce, inventory settings are defined at **Site Settings \> Extensions \> Inventory Management** in site builder.</span></span> <span data-ttu-id="bf365-116">Til eru fjórar birgðastillingar en ein þeirra er úreld:</span><span class="sxs-lookup"><span data-stu-id="bf365-116">There are four inventory settings, one of which is obsolete (deprecated):</span></span>

- <span data-ttu-id="bf365-117">**Virkja birgðaathugun í forriti** – Þessi stilling kveikir á birgðaathugun afurðar.</span><span class="sxs-lookup"><span data-stu-id="bf365-117">**Enable inventory check on app** – This setting turns on a product inventory check.</span></span> <span data-ttu-id="bf365-118">Einingarnar kaupgluggi og sækja í verslun athuga þá birgðir afurðar og leyfa að afurð sé bætt í körfuna aðeins ef birgðir eru til staðar.</span><span class="sxs-lookup"><span data-stu-id="bf365-118">Buy box, cart, and pick up in store modules will then check product inventory, and will allow a product to be added to the cart only if inventory is available.</span></span>
- <span data-ttu-id="bf365-119">**Birgðastaða byggir á** – Þessi stilling skilgreinir hvernig birgðastöður eru reiknaðar.</span><span class="sxs-lookup"><span data-stu-id="bf365-119">**Inventory level based on** – This setting defines how inventory levels are calculated.</span></span> <span data-ttu-id="bf365-120">Tiltæk gildi eru **Samtals tiltækt**, **Efnislegt magn tiltækt** og **Þröskuldur fyrir ekki til á lager**.</span><span class="sxs-lookup"><span data-stu-id="bf365-120">The available values are **Total Available**, **Physical Available**, and **Out of stock threshold**.</span></span> <span data-ttu-id="bf365-121">Í Commerce er hægt að skilgreina birgðaþröskuld og birgðabil fyrir hverja afurð og flokk.</span><span class="sxs-lookup"><span data-stu-id="bf365-121">In Commerce, inventory threshold and ranges can be defined for each product and category.</span></span> <span data-ttu-id="bf365-122">API-birgðir skila birgðaupplýsingum um afurð fyrir bæði eiginleikann **Samtals tiltækt** og **Efnislegt magn tiltækt**.</span><span class="sxs-lookup"><span data-stu-id="bf365-122">The inventory APIs return product inventory information for both the **Total Available** property and the **Physical Available** property.</span></span> <span data-ttu-id="bf365-123">Smásöluaðilinn ákveður hvort nota eigi **Samtals tiltækt** eða **Efnislegt magn tiltækt** til að ákvarða birgðatalninguna og samsvarandi bil fyrir „til á lager“ og „ekki til á lager“ stöðurnar.</span><span class="sxs-lookup"><span data-stu-id="bf365-123">The retailer decides whether the **Total Available** or **Physical Available** value should be used to determine the inventory count and the corresponding ranges for in-stock and out-of-stock statuses.</span></span>

    <span data-ttu-id="bf365-124">Gildið **Þröskuldur fyrir ekki til á lager** í stillingunni **Birgðastaða byggir á** er gamalt, úrelt gildi.</span><span class="sxs-lookup"><span data-stu-id="bf365-124">The **Out of stock threshold** value of the **Inventory level based on** setting is an old (legacy), obsolete value.</span></span> <span data-ttu-id="bf365-125">Þegar það er valið er birgðatalningin ákvörðuð út frá niðurstöðum gildisins **Samtals tiltækt**, en þröskuldurinn er skilgreindur af talnastillingunni **Þröskuldur fyrir ekki til á lager** sem er útskýrð seinna.</span><span class="sxs-lookup"><span data-stu-id="bf365-125">When it's selected, the inventory count is determined from the results of the **Total Available** value, but the threshold is defined by the **Out of stock threshold** numeric setting that is described later.</span></span> <span data-ttu-id="bf365-126">Þessi þröskuldsstilling á við um allar afurðir á svæði rafrænna viðskipta.</span><span class="sxs-lookup"><span data-stu-id="bf365-126">This threshold setting applies to all products across an e-Commerce site.</span></span> <span data-ttu-id="bf365-127">Ef birgðir eru undir þröskuldstölunni er litið á að afurð sé ekki til á lager.</span><span class="sxs-lookup"><span data-stu-id="bf365-127">If inventory is below the threshold number, a product is considered out of stock.</span></span> <span data-ttu-id="bf365-128">Annars er það talið til á lager.</span><span class="sxs-lookup"><span data-stu-id="bf365-128">Otherwise, it's considered in stock.</span></span> <span data-ttu-id="bf365-129">Möguleikar gildisins **Þröskuldur fyrir ekki til á lager** eru takmarkaðir og ekki er mælt með því að það sé notað í útgáfu 10.0.12 eða síðar.</span><span class="sxs-lookup"><span data-stu-id="bf365-129">The capabilities of the **Out of stock threshold** value are limited, and we don't recommend that you use it in version 10.0.12 and later.</span></span>

- <span data-ttu-id="bf365-130">**Birgðasvið** – Þessi stilling skilgreinir birgðasviðin sem skilaboð eru sýnd fyrir í einingum svæðis.</span><span class="sxs-lookup"><span data-stu-id="bf365-130">**Inventory ranges** – This setting defines the inventory ranges that message are shown for on site modules.</span></span> <span data-ttu-id="bf365-131">Það gildir aðeins ef annaðhvort gildið **Samtals tiltækt** eða gildið **Efnislegt magn tiltækt** er valið fyrir stillinguna **Birgðastaða byggist á**.</span><span class="sxs-lookup"><span data-stu-id="bf365-131">It's applicable only if either the **Total Available** value or the **Physical Available** value is selected for the **Inventory level based on** setting.</span></span> <span data-ttu-id="bf365-132">Tiltæk gildi eru **Allt**, **Litlar birgðir og ekki til á lager** og **Ekki til á lager**.</span><span class="sxs-lookup"><span data-stu-id="bf365-132">The available values are **All**, **Low and out of stock**, and **Out of stock**.</span></span>

    - <span data-ttu-id="bf365-133">Þegar **Allt** er valið verða skilaboð fyrir öll birgðasvið, frá á lager („Til á lager“ skilaboð) til ekki til á lager („Ekki til á lager“ skilaboð) sýnd.</span><span class="sxs-lookup"><span data-stu-id="bf365-133">When **All** is selected, messages for all inventory ranges, from in stock ("Available" message) to out of stock ("Out of stock" message), will be shown.</span></span>
    - <span data-ttu-id="bf365-134">Þegar **Litlar birgðir og ekki til á lager** er valið verða skilaboð fyrir öll birgðasvið, nema á lager („Til á lager“ skilaboð) sýnd.</span><span class="sxs-lookup"><span data-stu-id="bf365-134">When **Low and out of stock** is selected, messages for all inventory ranges except in stock ("Available" message) will be shown.</span></span>
    - <span data-ttu-id="bf365-135">Þegar **Ekki til á lager** er valið verður aðeins „Ekki til á lager“ skilaboðin sýnd.</span><span class="sxs-lookup"><span data-stu-id="bf365-135">When **Out of stock** is selected, only the "Out of stock" message will be shown.</span></span>

- <span data-ttu-id="bf365-136">**Þröskuldur fyrir ekki til á lager** - Þessi gamla talnastilling tekur aðeins gildi ef gildið **Þröskuldur fyrir ekki til á lager** er valið fyrir stillinguna **Birgðastaða byggist á**.</span><span class="sxs-lookup"><span data-stu-id="bf365-136">**Out of stock threshold** – This old numeric setting will take effect only if the **Out of stock threshold** value is selected for the **Inventory level based on** setting.</span></span>

## <a name="modules-that-use-inventory-settings"></a><span data-ttu-id="bf365-137">Einingar sem nota birgðastillingar</span><span class="sxs-lookup"><span data-stu-id="bf365-137">Modules that use inventory settings</span></span>

<span data-ttu-id="bf365-138">Einingarnar kaupgluggi, óskalisti, verslunarval, karfa og körfutákn nota birgðastillingar til að sýna birgðasviðin og skilaboðin.</span><span class="sxs-lookup"><span data-stu-id="bf365-138">Buy box, wishlist, store selector, cart, and cart icon modules use inventory settings to show the inventory ranges and messages.</span></span>

<span data-ttu-id="bf365-139">Eftirfarandi mynd sýnir dæmi um upplýsingasíðu afurðar sem sýnir á lager („Tiltækt“) skilaboðin.</span><span class="sxs-lookup"><span data-stu-id="bf365-139">The following image shows an example of a product details page (PDP) that is showing an in-stock ("Available") message.</span></span>

![Dæmi um upplýsingasíðu afurðar sem er með skilaboðin á lager](./media/pdp-InStock.png)

<span data-ttu-id="bf365-141">Eftirfarandi mynd sýnir dæmi um upplýsingasíðu afurðar sem sýnir „ekki til á lager“ skilaboðin.</span><span class="sxs-lookup"><span data-stu-id="bf365-141">The following image shows an example of a PDP that is showing an "Out of stock" message.</span></span>

![Dæmi um upplýsingasíðu afurðar sem er með skilaboðin ekki til á lager](./media/pdp-outofstock.png)

<span data-ttu-id="bf365-143">Eftirfarandi mynd sýnir dæmi um körfu sem sýnir skilaboðin til á lager („Tiltækt“).</span><span class="sxs-lookup"><span data-stu-id="bf365-143">The following image shows an example of a cart that is showing an in-stock ("Available") message.</span></span>

![Dæmi um körfueiningu sem er með skilaboðin til á lager](./media/cart-instock.png)

## <a name="additional-resources"></a><span data-ttu-id="bf365-145">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="bf365-145">Additional resources</span></span>

[<span data-ttu-id="bf365-146">Yfirlit byrjendaeiningar</span><span class="sxs-lookup"><span data-stu-id="bf365-146">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="bf365-147">Stilla birgðabiðminni og birgðastöðu</span><span class="sxs-lookup"><span data-stu-id="bf365-147">Configure inventory buffers and inventory levels</span></span>](inventory-buffers-levels.md)

[<span data-ttu-id="bf365-148">Körfueining</span><span class="sxs-lookup"><span data-stu-id="bf365-148">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="bf365-149">Kaupgluggaeining</span><span class="sxs-lookup"><span data-stu-id="bf365-149">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="bf365-150">Síður og einingar fyrir stjórnun reikninga</span><span class="sxs-lookup"><span data-stu-id="bf365-150">Account management pages and modules</span></span>](account-management.md)

[<span data-ttu-id="bf365-151">Vista valeiningu</span><span class="sxs-lookup"><span data-stu-id="bf365-151">Store selector module</span></span>](store-selector.md)
