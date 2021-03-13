---
title: Stilla takmörk afurðarmagns fyrir rafræn B2B-vefsvæði
description: Þetta efnisatriði lýsir hvernig á að stilla takmörk afurðarmagns fyrir B2B-vefsvæði rafrænna viðskipta.
author: josaw1
manager: AnnBe
ms.date: 01/20/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailOperations
audience: Application User, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: josaw
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: e70648da2cc1c526625b6e34fd0867d40abb5a85
ms.sourcegitcommit: f9df202aefef761be52c0360b0e22da88773914c
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/21/2021
ms.locfileid: "5035922"
---
# <a name="set-product-quantity-limits-for-b2b-e-commerce-sites"></a><span data-ttu-id="dc6fb-103">Stilla takmörk afurðarmagns fyrir rafræn B2B-vefsvæði</span><span class="sxs-lookup"><span data-stu-id="dc6fb-103">Set product quantity limits for B2B e-commerce sites</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="dc6fb-104">Þetta efnisatriði lýsir hvernig á að stilla takmörk afurðarmagns fyrir B2B-vefsvæði rafrænna viðskipta.</span><span class="sxs-lookup"><span data-stu-id="dc6fb-104">This topic describes how to set product quantity limits for business-to-business (B2B) e-commerce sites.</span></span>

<span data-ttu-id="dc6fb-105">Flestar afurðir eru með mælieiningu sem skilgreinir flokkun þeirra.</span><span class="sxs-lookup"><span data-stu-id="dc6fb-105">Most products have a unit of measure that defines their grouping.</span></span> <span data-ttu-id="dc6fb-106">Flokkunin hefur áhrif á það hvernig hægt er að selja afurðirnar.</span><span class="sxs-lookup"><span data-stu-id="dc6fb-106">The grouping affects how the products can be sold.</span></span> <span data-ttu-id="dc6fb-107">Sumar afurðir gætu verið með viðbótarflokkun fyrir magn.</span><span class="sxs-lookup"><span data-stu-id="dc6fb-107">Some products might have an additional grouping for quantities.</span></span> <span data-ttu-id="dc6fb-108">Þessi flokkun ákvarðar hvort hægt er að selja afurðirnar sem stakar einingar eða margar og hvort það er lágmark eða hámark á pöntunarmagni sem þarf að fylgja eftir.</span><span class="sxs-lookup"><span data-stu-id="dc6fb-108">This grouping determines whether the products can be sold as individual units or multiples, and whether there is a minimum or maximum order quantity limit that must be followed.</span></span>

<span data-ttu-id="dc6fb-109">Eiginleikinn fyrir takmörkun á magni tryggir að lágmarks- eða hámarksmagn, margar afurðir eða staðlað magn sem er skilgreint í Microsoft Dynamics 365 Commerce (í sjálfgefnum pöntunarstillingum eða í svæðisstillingum Commerce-vefsmiðs) verði notað í pöntunum viðskiptavina sem eru gerðar á svæði fyrir rafræn viðskipti.</span><span class="sxs-lookup"><span data-stu-id="dc6fb-109">The quantity limiting feature ensures that the minimum, maximum, multiple, and standard quantities that are configured in Microsoft Dynamics 365 Commerce (in the default order settings or the Commerce site builder site settings) are applied to customer orders that are placed on an e-commerce site.</span></span> <span data-ttu-id="dc6fb-110">Takmörk afurðarmagns eru ekki studd sem stendur fyrir sölustað og símaver.</span><span class="sxs-lookup"><span data-stu-id="dc6fb-110">Product quantity limits aren't currently supported for the point of sale (POS) and call centers.</span></span>

<span data-ttu-id="dc6fb-111">Margir smásalar bjóða upp á valkost viðskiptavinapantana (einnig þekkt sem sérpantanir) til að mæta ýmsum þörfum afurða og uppfyllingar.</span><span class="sxs-lookup"><span data-stu-id="dc6fb-111">Many retailers provide the option of customer orders (also known as special orders) to meet various product and fulfillment requirements.</span></span> <span data-ttu-id="dc6fb-112">Hér eru nokkrar dæmigerðar aðstæður.</span><span class="sxs-lookup"><span data-stu-id="dc6fb-112">Here are some typical scenarios:</span></span>

- <span data-ttu-id="dc6fb-113">Viðskiptavinur vill að afurðir af tilteknum afbrigðum verði seldar nokkrar í einu.</span><span class="sxs-lookup"><span data-stu-id="dc6fb-113">A customer wants products of specific variants to be sold in multiples of a few.</span></span>
- <span data-ttu-id="dc6fb-114">Viðskiptavinur vill taka til afurðir úr verslun eða staðsetningu sem er önnur en verslunin eða staðsetningin þar sem viðskiptamaðurinn keypti þær afurðir.</span><span class="sxs-lookup"><span data-stu-id="dc6fb-114">A customer wants to pick up products from a store or location that differs from the store or location where the customer purchased those products.</span></span> <span data-ttu-id="dc6fb-115">Hins vegar eru pökkunarstaðlar fyrir verslanirnar ólíkir pökkunarstöðlum söludreifingar á netinu.</span><span class="sxs-lookup"><span data-stu-id="dc6fb-115">However, the packing standards for the stores differ from the packing standards for online sales distribution.</span></span>
- <span data-ttu-id="dc6fb-116">Viðskiptavinur vill kaupa afurð í takmörkuðu upplagi sem er með hámarksmagn fyrir vörur sem má kaupa.</span><span class="sxs-lookup"><span data-stu-id="dc6fb-116">A customer wants to buy a limited-edition product that has a maximum quantity limit for items that can be purchased.</span></span>

## <a name="turn-on-the-default-order-settings-feature-in-commerce-headquarters"></a><span data-ttu-id="dc6fb-117">Kveikja á eiginleika sjálfgefinna pöntunarstillinga í Commerce Headquarters</span><span class="sxs-lookup"><span data-stu-id="dc6fb-117">Turn on the default order settings feature in Commerce headquarters</span></span>

<span data-ttu-id="dc6fb-118">Áður en hægt er að stilla takmarkanir á afurðarmagni þarf að kveikja á eiginleika sjálfgefinna pöntunarstillinga í Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="dc6fb-118">Before you can set product quantity limits, the default order settings feature must be turned on in Commerce headquarters.</span></span>

<span data-ttu-id="dc6fb-119">Til að kveikja á eiginleika sjálfgefinna pöntunarstillinga skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="dc6fb-119">To turn on the default order settings feature, follow these steps.</span></span>

1. <span data-ttu-id="dc6fb-120">Opna skal **Kerfisstjórnun \> Vinnusvæði \> Eiginleikastjórnun**.</span><span class="sxs-lookup"><span data-stu-id="dc6fb-120">Go to **System administration \> Workspaces \> Feature management**.</span></span>
1. <span data-ttu-id="dc6fb-121">Finnið og veljið eiginleikann **Styðja svæðisstillingar og sjálfgefnar pöntunarstillingar í pöntun viðskiptavinar**.</span><span class="sxs-lookup"><span data-stu-id="dc6fb-121">Find and select the **Support the Site and Default order settings in the customer order** feature.</span></span>
1. <span data-ttu-id="dc6fb-122">Neðst í glugganum hægra megin skal velja **Virkja núna**.</span><span class="sxs-lookup"><span data-stu-id="dc6fb-122">At the bottom of the right pane, select **Enable now**.</span></span> 

## <a name="define-quantity-settings"></a><span data-ttu-id="dc6fb-123">Skilgreina magnstillingar</span><span class="sxs-lookup"><span data-stu-id="dc6fb-123">Define quantity settings</span></span> 

<span data-ttu-id="dc6fb-124">Hægt er að skilgreina magnstillingar á síðunni **Sjálfgefnar pöntunarstillingar**.</span><span class="sxs-lookup"><span data-stu-id="dc6fb-124">You can define the quantity settings on the **Default order settings** page.</span></span>

<span data-ttu-id="dc6fb-125">Til að skilgreina magnstillingar skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="dc6fb-125">To define the quantity settings, follow these steps.</span></span> 

1. <span data-ttu-id="dc6fb-126">Farið í **Smásala og viðskipti \> Afurðir og tegundir \> Losaðar afurðir eftir flokki**.</span><span class="sxs-lookup"><span data-stu-id="dc6fb-126">Go to Product **Retail and Commerce \> Products and categories \> Released products by category**.</span></span>
1. <span data-ttu-id="dc6fb-127">Veljið útgefna afurð.</span><span class="sxs-lookup"><span data-stu-id="dc6fb-127">Select a released product.</span></span>
1. <span data-ttu-id="dc6fb-128">Á aðgerðasvæðinu, í flipanum **Stjórna birgðum**, í flokknum **Pöntunarstillingar**, skal velja **Sjálfgefnar pöntunarstillingar**.</span><span class="sxs-lookup"><span data-stu-id="dc6fb-128">On the Action Pane, on the **Manage inventory** tab, in the **Order settings** group, select **Default order settings**.</span></span> 
1. <span data-ttu-id="dc6fb-129">Á síðunni **Sjálfgefnar pöntunarstillingar**, í flýtiflipanum **Sölupöntun**, í hlutanum **Sölumagn**, skal stilla sölumagn afurðar:</span><span class="sxs-lookup"><span data-stu-id="dc6fb-129">On the **Default order settings** page, on the **Sales order** FastTab, in the **Sales quantity** section, set the product sales quantities:</span></span>

    - <span data-ttu-id="dc6fb-130">**Margfeldi** – Magnið sem hægt er að kaupa afurðina í margfeldi af.</span><span class="sxs-lookup"><span data-stu-id="dc6fb-130">**Multiple** – The quantity that the product can be bought in multiples of.</span></span>
    - <span data-ttu-id="dc6fb-131">**Lágmarksmagn pöntunar** – Lágmarksfjöldi afurða sem þarf að kaupa.</span><span class="sxs-lookup"><span data-stu-id="dc6fb-131">**Minimum Order Quantity** – The minimum number of products that must be purchased.</span></span>
    - <span data-ttu-id="dc6fb-132">**Hámarksmagn pöntunar** – Hámarksfjöldi afurða sem hægt er að kaupa.</span><span class="sxs-lookup"><span data-stu-id="dc6fb-132">**Maximum Order Quantity** – The maximum number of products that can be purchased.</span></span>
    - <span data-ttu-id="dc6fb-133">**Staðlað pöntunarmagn** – Sjálfgefið magn sem sjálfkrafa er fært inn þegar afurðin er valin.</span><span class="sxs-lookup"><span data-stu-id="dc6fb-133">**Standard Order Quantity** – The default quantity that is automatically entered when the product is selected.</span></span>

## <a name="turn-on-the-b2b-order-quantity-limits-feature-in-commerce-site-builder"></a><span data-ttu-id="dc6fb-134">Kveikja á eiginleika fyrir takmörk B2B-pöntunarmagns í Commerce-vefsmið</span><span class="sxs-lookup"><span data-stu-id="dc6fb-134">Turn on the B2B order quantity limits feature in Commerce site builder</span></span>

<span data-ttu-id="dc6fb-135">Til að kveikja á eiginleika fyrir takmörk B2B-pöntunarmagns í Commerce-vefsmið skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="dc6fb-135">To turn on the B2B order quantity limits feature in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="dc6fb-136">Farið í **Svæðisstillingar \> Viðbætur**</span><span class="sxs-lookup"><span data-stu-id="dc6fb-136">Go to **Site settings \> Extensions**</span></span>
1. <span data-ttu-id="dc6fb-137">Undir **Virkja takmörk pöntunarmagns** skal velja **Virkjað fyrir B2B-viðskiptavini** í fellivalmyndinni.</span><span class="sxs-lookup"><span data-stu-id="dc6fb-137">Under **Enable Order Quantity Limits**, select **Enabled for B2B customers** in the drop-down menu.</span></span> 

> [!NOTE] 
> <span data-ttu-id="dc6fb-138">Uppfærðar stillingar vefsmiðs taka fyrst gildi eftir að skráin app.settings.json hefur verið uppfærð.</span><span class="sxs-lookup"><span data-stu-id="dc6fb-138">Updated site builder settings take effect only after the app.settings.json file has been updated.</span></span> <span data-ttu-id="dc6fb-139">Frekari upplýsingar er að finna í [Uppfærslur á SDK og einingasafni](../e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span><span class="sxs-lookup"><span data-stu-id="dc6fb-139">For more information, see [SDK and Module library updates](../e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="dc6fb-140">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="dc6fb-140">Additional resources</span></span>

[<span data-ttu-id="dc6fb-141">Setja upp B2B-svæði fyrir rafræn viðskipti</span><span class="sxs-lookup"><span data-stu-id="dc6fb-141">Set up a B2B e-commerce site</span></span>](set-up-b2b-site.md)

[<span data-ttu-id="dc6fb-142">Stofna líkanastigveldi fyrir B2B-fyrirtæki</span><span class="sxs-lookup"><span data-stu-id="dc6fb-142">Create org modeling hierarchies for B2B organizations</span></span>](org-model.md)

[<span data-ttu-id="dc6fb-143">Stjórna notendum viðskiptafélaga á B2B-svæði fyrir rafræn viðskipti</span><span class="sxs-lookup"><span data-stu-id="dc6fb-143">Manage business partner users on B2B e-commerce sites</span></span>](manage-b2b-users.md)

[<span data-ttu-id="dc6fb-144">Skilgreina greiðslumáta viðskiptavinalykils fyrir B2B-svæði fyrir rafræn viðskipti</span><span class="sxs-lookup"><span data-stu-id="dc6fb-144">Configure the customer account payment method for B2B e-commerce sites</span></span>](payment-method.md)
