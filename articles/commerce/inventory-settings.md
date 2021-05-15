---
title: Nota birgðastillingar
description: Í efnisatriði er fjallað um birgðastillingar og útskýrt hvernig á að nota þær í Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 04/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: dd3db0039525c18521ad6a42b2f281976b7b236a
ms.sourcegitcommit: 593438a145672c55ff6a910eabce2939300b40ad
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/23/2021
ms.locfileid: "5937411"
---
# <a name="apply-inventory-settings"></a><span data-ttu-id="f152e-103">Nota birgðastillingar</span><span class="sxs-lookup"><span data-stu-id="f152e-103">Apply inventory settings</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="f152e-104">Í efnisatriði er fjallað um birgðastillingar og útskýrt hvernig á að nota þær í Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="f152e-104">This topic covers inventory settings and describes how to apply them in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="f152e-105">Birgðastillingar tilgreina hvort athuga eigi birgða áður en afurðir eru settar í körfuna.</span><span class="sxs-lookup"><span data-stu-id="f152e-105">Inventory settings specify whether inventory should be checked before products are added to the cart.</span></span> <span data-ttu-id="f152e-106">Þær skilgreina einnig birgðatengd skilaboð um smásöluvörur, t.d. „Á lager“ og „Lítið eftir“.</span><span class="sxs-lookup"><span data-stu-id="f152e-106">They also define inventory-related merchandising messages, such as "In stock" and "Only a few left."</span></span> <span data-ttu-id="f152e-107">Þessar stillingar ganga úr skugga um að ekki sé hægt að kaupa afurð ef hún er ekki til á lager.</span><span class="sxs-lookup"><span data-stu-id="f152e-107">These settings ensure that a product can't be purchased if it's out of stock.</span></span>

<span data-ttu-id="f152e-108">Dynamics 365 Commerce leggur mat á lagerstöðu fyrir afurðir.</span><span class="sxs-lookup"><span data-stu-id="f152e-108">Dynamics 365 Commerce provides estimates of on-hand availability for products.</span></span> <span data-ttu-id="f152e-109">Upplýsingar um hvernig áætlað framboð á lager er reiknað er að finna í [Reikna tiltækar birgðir fyrir smásölurásir](calculated-inventory-retail-channels.md).</span><span class="sxs-lookup"><span data-stu-id="f152e-109">For information about how estimated on-hand availability is calculated, see [Calculate inventory availability for retail channels](calculated-inventory-retail-channels.md).</span></span>

<span data-ttu-id="f152e-110">Í Commerce-vefssmið er hægt að skilgreina birgðaþröskuld og birgðabil fyrir afurð eða flokk.</span><span class="sxs-lookup"><span data-stu-id="f152e-110">In Commerce site builder, inventory thresholds and ranges can be defined for a product or a category.</span></span> <span data-ttu-id="f152e-111">Það ákvarðar hvort birgðir geti verið flokkaðar sem á lager, lítið til á lager eða ekki til á lager.</span><span class="sxs-lookup"><span data-stu-id="f152e-111">They determine whether inventory can be classified as in stock, low stock, or out of stock.</span></span> <span data-ttu-id="f152e-112">Frekari upplýsingar er að finna í [Stilla birgðabiðminni og birgðastöðu](inventory-buffers-levels.md).</span><span class="sxs-lookup"><span data-stu-id="f152e-112">For details, see [Configure inventory buffers and inventory levels](inventory-buffers-levels.md).</span></span>

> [!NOTE]
> <span data-ttu-id="f152e-113">Stuðningur við birgðaþröskulda og svið er tiltækur í Dynamics 365 Commerce útgáfu 10.0.12.</span><span class="sxs-lookup"><span data-stu-id="f152e-113">Support for inventory thresholds and ranges is available in the Dynamics 365 Commerce 10.0.12 release.</span></span>

## <a name="inventory-settings"></a><span data-ttu-id="f152e-114">Birgðastillingar</span><span class="sxs-lookup"><span data-stu-id="f152e-114">Inventory settings</span></span>

<span data-ttu-id="f152e-115">Í Commerce eru birgðastillingar skilgreindar í **Stillingar svæðis \> Viðbætur \> Birgðastjórnun** í svæðissmið.</span><span class="sxs-lookup"><span data-stu-id="f152e-115">In Commerce, inventory settings are defined at **Site Settings \> Extensions \> Inventory Management** in site builder.</span></span> <span data-ttu-id="f152e-116">Til eru fimm birgðastillingar en ein þeirra er úreld:</span><span class="sxs-lookup"><span data-stu-id="f152e-116">There are five inventory settings, one of which is obsolete (deprecated):</span></span>

- <span data-ttu-id="f152e-117">**Virkja birgðaathugun í forriti** – Þessi stilling kveikir á birgðaathugun afurðar.</span><span class="sxs-lookup"><span data-stu-id="f152e-117">**Enable stock check in app** – This setting turns on a product inventory check.</span></span> <span data-ttu-id="f152e-118">Einingarnar kaupgluggi og sækja í verslun athuga þá birgðir afurðar og leyfa að afurð sé bætt í körfuna aðeins ef birgðir eru til staðar.</span><span class="sxs-lookup"><span data-stu-id="f152e-118">Buy box, cart, and pick up in store modules will then check product inventory, and will allow a product to be added to the cart only if inventory is available.</span></span>
- <span data-ttu-id="f152e-119">**Birgðastaða byggir á** – Þessi stilling skilgreinir hvernig birgðastöður eru reiknaðar.</span><span class="sxs-lookup"><span data-stu-id="f152e-119">**Inventory level based on** – This setting defines how inventory levels are calculated.</span></span> <span data-ttu-id="f152e-120">Tiltæk gildi eru **Samtals tiltækt**, **Efnislegt magn tiltækt** og **Þröskuldur fyrir ekki til á lager**.</span><span class="sxs-lookup"><span data-stu-id="f152e-120">The available values are **Total Available**, **Physical Available**, and **Out of stock threshold**.</span></span> <span data-ttu-id="f152e-121">Í Commerce er hægt að skilgreina birgðaþröskuld og birgðabil fyrir hverja afurð og flokk.</span><span class="sxs-lookup"><span data-stu-id="f152e-121">In Commerce, inventory threshold and ranges can be defined for each product and category.</span></span> <span data-ttu-id="f152e-122">API-birgðir skila birgðaupplýsingum um afurð fyrir bæði eiginleikann **Samtals tiltækt** og **Efnislegt magn tiltækt**.</span><span class="sxs-lookup"><span data-stu-id="f152e-122">The inventory APIs return product inventory information for both the **Total Available** property and the **Physical Available** property.</span></span> <span data-ttu-id="f152e-123">Smásöluaðilinn ákveður hvort nota eigi **Samtals tiltækt** eða **Efnislegt magn tiltækt** til að ákvarða birgðatalninguna og samsvarandi bil fyrir „til á lager“ og „ekki til á lager“ stöðurnar.</span><span class="sxs-lookup"><span data-stu-id="f152e-123">The retailer decides whether the **Total Available** or **Physical Available** value should be used to determine the inventory count and the corresponding ranges for in-stock and out-of-stock statuses.</span></span>

    <span data-ttu-id="f152e-124">Gildið **Þröskuldur fyrir ekki til á lager** í stillingunni **Birgðastaða byggir á** er gamalt, úrelt gildi.</span><span class="sxs-lookup"><span data-stu-id="f152e-124">The **Out of stock threshold** value of the **Inventory level based on** setting is an old (legacy), obsolete value.</span></span> <span data-ttu-id="f152e-125">Þegar það er valið er birgðatalningin ákvörðuð út frá niðurstöðum gildisins **Samtals tiltækt**, en þröskuldurinn er skilgreindur af talnastillingunni **Þröskuldur fyrir ekki til á lager** sem er útskýrð seinna.</span><span class="sxs-lookup"><span data-stu-id="f152e-125">When it's selected, the inventory count is determined from the results of the **Total Available** value, but the threshold is defined by the **Out of stock threshold** numeric setting that is described later.</span></span> <span data-ttu-id="f152e-126">Þessi þröskuldsstilling á við um allar afurðir á svæði rafrænna viðskipta.</span><span class="sxs-lookup"><span data-stu-id="f152e-126">This threshold setting applies to all products across an e-commerce site.</span></span> <span data-ttu-id="f152e-127">Ef birgðir eru undir þröskuldstölunni er litið á að afurð sé ekki til á lager.</span><span class="sxs-lookup"><span data-stu-id="f152e-127">If inventory is below the threshold number, a product is considered out of stock.</span></span> <span data-ttu-id="f152e-128">Annars er það talið til á lager.</span><span class="sxs-lookup"><span data-stu-id="f152e-128">Otherwise, it's considered in stock.</span></span> <span data-ttu-id="f152e-129">Möguleikar gildisins **Þröskuldur fyrir ekki til á lager** eru takmarkaðir og ekki er mælt með því að það sé notað í útgáfu 10.0.12 eða síðar.</span><span class="sxs-lookup"><span data-stu-id="f152e-129">The capabilities of the **Out of stock threshold** value are limited, and we don't recommend that you use it in version 10.0.12 and later.</span></span>

- <span data-ttu-id="f152e-130">**Birgðastig fyrir mörg vöruhús** – Þessi stilling gerir kleift að reikna birgðastöðuna gagnvart sjálfgefnu vöruhúsi eða mörgum vöruhúsum.</span><span class="sxs-lookup"><span data-stu-id="f152e-130">**Inventory level for multiple warehouses** – This setting enables the inventory level to be calculated against the default warehouse or multiple warehouses.</span></span> <span data-ttu-id="f152e-131">Valkosturinn **Byggt á einu vöruhúsi** mun reikna út birgðastöðuna út frá sjálfgefna vöruhúsinu.</span><span class="sxs-lookup"><span data-stu-id="f152e-131">The **Based on individual warehouse** option will calculate inventory levels based on the default warehouse.</span></span> <span data-ttu-id="f152e-132">Einnig getur svæði rafrænna viðskipta bent á mörg vöruhús til að auðvelda uppfyllingu.</span><span class="sxs-lookup"><span data-stu-id="f152e-132">Alternatively, an e-commerce site can point to multiple warehouses to facilitate fulfillment.</span></span> <span data-ttu-id="f152e-133">Í því tilfelli er valkosturinn **Byggt á samtölu fyrir vöruhús sendingar og afhendingar** notaður til að gefa til kynna birgðaframboð.</span><span class="sxs-lookup"><span data-stu-id="f152e-133">In that case, the **Based on aggregate for Shipping and Pickup warehouses** option is used to indicate stock availability.</span></span> <span data-ttu-id="f152e-134">Til dæmis þegar viðskiptavinur kaupir vöru og velur „sendingu“ sem afhendingarmátann, varan getur verið send frá einhverju vöruhúsi í uppfyllingarflokknum sem er með birgðir á lausu.</span><span class="sxs-lookup"><span data-stu-id="f152e-134">For example, when a customer purchases an item and selects "shipping" as the delivery mode, the item can be shipped from any warehouse in the fulfillment group that has available inventory.</span></span> <span data-ttu-id="f152e-135">Upplýsingasíða afurðar (PDP) mun sýna skilaboðin „Á lager“ fyrir sendingu ef eitthvert vöruhús sendingar í uppfyllingarflokknum er með birgðir.</span><span class="sxs-lookup"><span data-stu-id="f152e-135">The product details page (PDP) will show an "In stock" message for shipping if any available shipping warehouse in the fulfillment group has inventory.</span></span> 

> [!IMPORTANT] 
> <span data-ttu-id="f152e-136">Stillingin **Birgðastaða fyrir mörg vöruhús** er í boði frá og með Commerce-útgáfu 10.0.19.</span><span class="sxs-lookup"><span data-stu-id="f152e-136">The **Inventory level for multiple warehouses** setting is available as of the Commerce version 10.0.19 release.</span></span> <span data-ttu-id="f152e-137">Ef verið er að uppfæra úr eldri útgáfu af Commerce verður að uppfæra appsettings.json-skrána handvirkt.</span><span class="sxs-lookup"><span data-stu-id="f152e-137">If you're updating from an older version of Commerce, you must manually update the appsettings.json file.</span></span> <span data-ttu-id="f152e-138">Leiðbeiningar er að finna í [Uppfærslur á SDK og einingasafni](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span><span class="sxs-lookup"><span data-stu-id="f152e-138">For instructions, see [SDK and module library updates](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span></span>

- <span data-ttu-id="f152e-139">**Birgðasvið** – Þessi stilling skilgreinir birgðasviðin sem skilaboð eru sýnd fyrir í einingum svæðis.</span><span class="sxs-lookup"><span data-stu-id="f152e-139">**Inventory ranges** – This setting defines the inventory ranges that message are shown for on site modules.</span></span> <span data-ttu-id="f152e-140">Það gildir aðeins ef annaðhvort gildið **Samtals tiltækt** eða gildið **Efnislegt magn tiltækt** er valið fyrir stillinguna **Birgðastaða byggist á**.</span><span class="sxs-lookup"><span data-stu-id="f152e-140">It's applicable only if either the **Total Available** value or the **Physical Available** value is selected for the **Inventory level based on** setting.</span></span> <span data-ttu-id="f152e-141">Tiltæk gildi eru **Allt**, **Litlar birgðir og ekki til á lager** og **Ekki til á lager**.</span><span class="sxs-lookup"><span data-stu-id="f152e-141">The available values are **All**, **Low and out of stock**, and **Out of stock**.</span></span>

    - <span data-ttu-id="f152e-142">Þegar **Allt** er valið verða skilaboð fyrir öll birgðasvið, frá á lager („Til á lager“ skilaboð) til ekki til á lager („Ekki til á lager“ skilaboð) sýnd.</span><span class="sxs-lookup"><span data-stu-id="f152e-142">When **All** is selected, messages for all inventory ranges, from in stock ("Available" message) to out of stock ("Out of stock" message), will be shown.</span></span>
    - <span data-ttu-id="f152e-143">Þegar **Litlar birgðir og ekki til á lager** er valið verða skilaboð fyrir öll birgðasvið, nema á lager („Til á lager“ skilaboð) sýnd.</span><span class="sxs-lookup"><span data-stu-id="f152e-143">When **Low and out of stock** is selected, messages for all inventory ranges except in stock ("Available" message) will be shown.</span></span>
    - <span data-ttu-id="f152e-144">Þegar **Ekki til á lager** er valið verður aðeins „Ekki til á lager“ skilaboðin sýnd.</span><span class="sxs-lookup"><span data-stu-id="f152e-144">When **Out of stock** is selected, only the "Out of stock" message will be shown.</span></span>

- <span data-ttu-id="f152e-145">**Þröskuldur fyrir ekki til á lager** - Þessi gamla talnastilling tekur aðeins gildi ef gildið **Þröskuldur fyrir ekki til á lager** er valið fyrir stillinguna **Birgðastaða byggist á**.</span><span class="sxs-lookup"><span data-stu-id="f152e-145">**Out of stock threshold** – This old numeric setting will take effect only if the **Out of stock threshold** value is selected for the **Inventory level based on** setting.</span></span>

> [!IMPORTANT] 
> <span data-ttu-id="f152e-146">Þessar stillingar eru í boði í Dynamics 365 Commerce útgáfu 10.0.12.</span><span class="sxs-lookup"><span data-stu-id="f152e-146">These settings are available in the Dynamics 365 Commerce 10.0.12 release.</span></span> <span data-ttu-id="f152e-147">Ef verið er að uppfæra úr eldri útgáfu af Dynamics 365 Commerce verður að uppfæra appsettings.json-skrána handvirkt.</span><span class="sxs-lookup"><span data-stu-id="f152e-147">If you are updating from an older version of Dynamics 365 Commerce, you must manually update the appsettings.json file.</span></span> <span data-ttu-id="f152e-148">Leiðbeiningar um uppfærslu appsettings.json skrárinnar er að finna í [Uppfærslur á SDK og einingasafni](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span><span class="sxs-lookup"><span data-stu-id="f152e-148">For instructions on updating the appsettings.json file, see [SDK and module library updates](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span></span>

## <a name="modules-that-use-inventory-settings"></a><span data-ttu-id="f152e-149">Einingar sem nota birgðastillingar</span><span class="sxs-lookup"><span data-stu-id="f152e-149">Modules that use inventory settings</span></span>

<span data-ttu-id="f152e-150">Einingarnar kaupgluggi, óskalisti, verslunarval, karfa og körfutákn nota birgðastillingar til að sýna birgðasviðin og skilaboðin.</span><span class="sxs-lookup"><span data-stu-id="f152e-150">Buy box, wishlist, store selector, cart, and cart icon modules use inventory settings to show the inventory ranges and messages.</span></span>

<span data-ttu-id="f152e-151">Í dæminu á eftirfarandi mynd sýnir PDP lagerskilaboð („Tiltækt“).</span><span class="sxs-lookup"><span data-stu-id="f152e-151">In the example in the following illustration, a PDP is showing an in-stock ("Available") message.</span></span>

![Dæmi um upplýsingasíðu afurðar sem er með skilaboðin á lager](./media/pdp-InStock.png)

<span data-ttu-id="f152e-153">Í dæminu á eftirfarandi mynd sýnir PDP skilaboðin „Ekki til á lager“.</span><span class="sxs-lookup"><span data-stu-id="f152e-153">In the example in the following illustration, a PDP is showing an "Out of stock" message.</span></span>

![Dæmi um upplýsingasíðu afurðar sem er með skilaboðin ekki til á lager](./media/pdp-outofstock.png)

<span data-ttu-id="f152e-155">Í dæminu á eftirfarandi mynd sýnir karfa lagerskilaboð („Tiltækt“).</span><span class="sxs-lookup"><span data-stu-id="f152e-155">In the example in the following illustration, a cart is showing an in-stock ("Available") message.</span></span>

![Dæmi um körfueiningu sem er með skilaboðin til á lager](./media/cart-instock.png)

## <a name="additional-resources"></a><span data-ttu-id="f152e-157">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="f152e-157">Additional resources</span></span>

[<span data-ttu-id="f152e-158">Yfirlit einingasafns</span><span class="sxs-lookup"><span data-stu-id="f152e-158">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="f152e-159">Skilgreina birgðabiðminni og birgðastöðu</span><span class="sxs-lookup"><span data-stu-id="f152e-159">Configure inventory buffers and inventory levels</span></span>](inventory-buffers-levels.md)

[<span data-ttu-id="f152e-160">Körfueining</span><span class="sxs-lookup"><span data-stu-id="f152e-160">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="f152e-161">Kaupgluggaeining</span><span class="sxs-lookup"><span data-stu-id="f152e-161">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="f152e-162">Síður og einingar fyrir stjórnun reikninga</span><span class="sxs-lookup"><span data-stu-id="f152e-162">Account management pages and modules</span></span>](account-management.md)

[<span data-ttu-id="f152e-163">Eining til að velja verslun</span><span class="sxs-lookup"><span data-stu-id="f152e-163">Store selector module</span></span>](store-selector.md)

[<span data-ttu-id="f152e-164">Uppfærslur á SDK og kjarnasafni</span><span class="sxs-lookup"><span data-stu-id="f152e-164">SDK and module library updates</span></span>](e-commerce-extensibility/sdk-updates.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
