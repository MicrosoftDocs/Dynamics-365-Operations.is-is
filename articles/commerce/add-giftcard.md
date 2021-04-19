---
title: Gjafakortseining
description: Þetta efni fjallar um gjafakortseiningar og lýsir því hvernig á að bæta þeim við vefsíður hjá Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: a4e4e06ab7032d68fcd36a8e80bc714ebaaac821
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5797672"
---
# <a name="gift-card-module"></a><span data-ttu-id="fd801-103">Gjafakortseining</span><span class="sxs-lookup"><span data-stu-id="fd801-103">Gift card module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="fd801-104">Þetta efni fjallar um gjafakortseiningar og lýsir því hvernig á að bæta þeim við vefsíður hjá Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="fd801-104">This topic covers gift card modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="fd801-105">Hægt er að nota einingar gjafakorta við greiðslueiningar til að taka á móti gjafakortum, sem er algeng gerð greiðsla sem eru notaðar fyrir rafræn viðskipti.</span><span class="sxs-lookup"><span data-stu-id="fd801-105">Gift card modules can be used in checkout modules to accept gift cards, a common form of payment used for e-Commerce transactions.</span></span> <span data-ttu-id="fd801-106">Gjafakortseiningin styður Dynamics 365, SVS og Givex gjafakort.</span><span class="sxs-lookup"><span data-stu-id="fd801-106">The gift card module supports Dynamics 365, SVS, and Givex gift cards.</span></span> <span data-ttu-id="fd801-107">Gjafakort SVS og Givex eru innleyst með Adyen greiðsluþjónustuaðila.</span><span class="sxs-lookup"><span data-stu-id="fd801-107">SVS and Givex gift cards are redeemed via the Adyen payment provider.</span></span> <span data-ttu-id="fd801-108">Frekari upplýsingar um stuðning við gjafakort, svo sem SVS og Givex, eru í [Stuðningur við utanaðkomandi gjafakort](./dev-itpro/gift-card.md).</span><span class="sxs-lookup"><span data-stu-id="fd801-108">For more information about support for external gift cards such as SVS and Givex, see [Support for external gift cards](./dev-itpro/gift-card.md).</span></span>

> [!NOTE]
> <span data-ttu-id="fd801-109">Stuðningur við innlausn SVS og Givex-gjafakorta við greiðsluferli er í boði í Dynamics 365 Commerce útgáfu 10.0.11.</span><span class="sxs-lookup"><span data-stu-id="fd801-109">Support for redeeming SVS and Givex gift cards during checkout flow is available in the Dynamics 365 Commerce 10.0.11 release.</span></span> 

<span data-ttu-id="fd801-110">Tvær gjafakortseiningar eru í boði:</span><span class="sxs-lookup"><span data-stu-id="fd801-110">There are two gift card modules available:</span></span>

- <span data-ttu-id="fd801-111">**Gjafakort** - Hægt er að nota þessa einingu á greiðslusíðu til að innleysa gjafakort sem tilboð.</span><span class="sxs-lookup"><span data-stu-id="fd801-111">**Gift card** - This module can be used on a checkout page to redeem a gift card as tender.</span></span> 
- <span data-ttu-id="fd801-112">**Könnun á stöðu gjafakorts** - Hægt er að nota þessa einingu á hvaða síðu sem er til að skoða stöðuna á gjafakorti.</span><span class="sxs-lookup"><span data-stu-id="fd801-112">**Gift card balance check** - This module can be used on any page to check the balance on a gift card.</span></span> <span data-ttu-id="fd801-113">Þessi eining er tiltæk í Commerce Release 10.0.14 og nýrri.</span><span class="sxs-lookup"><span data-stu-id="fd801-113">This module is available in Commerce release 10.0.14 and later.</span></span>

> [!NOTE]
> <span data-ttu-id="fd801-114">Stuðningur við fyrir athugunarstöðu gjafakorts er tiltækur í Dynamics 365 Commerce útgáfu 10.0.14.</span><span class="sxs-lookup"><span data-stu-id="fd801-114">Support for the gift card balance check module is available in the Dynamics 365 Commerce 10.0.14 release.</span></span>

<span data-ttu-id="fd801-115">Eftirfarandi mynd sýnir dæmi um gjafakortseiningu á greiðsluferlissíðu.</span><span class="sxs-lookup"><span data-stu-id="fd801-115">The following image shows an example of a gift card module on a checkout page.</span></span>

![Dæmi um gjafakortseiningu](./media/ecommerce-giftcard.PNG)

## <a name="module-properties"></a><span data-ttu-id="fd801-117">Eiginleikar einingar</span><span class="sxs-lookup"><span data-stu-id="fd801-117">Module properties</span></span>

- <span data-ttu-id="fd801-118">**Sýna fleiri reiti** - Þessi eiginleiki skilgreinir hvaða reiti skuli birta fyrir gjafakort auk gjafakortsnúmersins sem er alltaf birt sjálfgefið.</span><span class="sxs-lookup"><span data-stu-id="fd801-118">**Show additional fields** - This property defines what fields should be displayed for gift cards in addition to the gift card number, which is always displayed by default.</span></span> <span data-ttu-id="fd801-119">Til dæmis styðja sum gjafakort með birtinu á persónuauðkenni (PIN) og önnur styðja birtingu PIN og gildistíma.</span><span class="sxs-lookup"><span data-stu-id="fd801-119">For example, some gift cards support displaying a personal identification number (PIN), and others support displaying a PIN and expiration date.</span></span> <span data-ttu-id="fd801-120">Að öðrum kosti væri hægt að stilla þennan eiginleika á „Enginn“, sem myndi aðeins sýna gjafakortsnúmerið og enga viðbótarreiti.</span><span class="sxs-lookup"><span data-stu-id="fd801-120">Alternatively, this property could be set to "None", which would only display the gift card number and no additional fields.</span></span>

<span data-ttu-id="fd801-121">Studd gildi:</span><span class="sxs-lookup"><span data-stu-id="fd801-121">Supported values:</span></span>
-   <span data-ttu-id="fd801-122">PIN</span><span class="sxs-lookup"><span data-stu-id="fd801-122">PIN</span></span>
-   <span data-ttu-id="fd801-123">Gildistími</span><span class="sxs-lookup"><span data-stu-id="fd801-123">Expiration date</span></span>
-   <span data-ttu-id="fd801-124">PIN og lokadagur</span><span class="sxs-lookup"><span data-stu-id="fd801-124">PIN and expiration date</span></span> 
-   <span data-ttu-id="fd801-125">None</span><span class="sxs-lookup"><span data-stu-id="fd801-125">None</span></span>

## <a name="site-settings-for-gift-card-modules"></a><span data-ttu-id="fd801-126">Vefstillingar fyrir gjafakortseiningar</span><span class="sxs-lookup"><span data-stu-id="fd801-126">Site settings for gift card modules</span></span>

<span data-ttu-id="fd801-127">Í vefsvæðishönnuði Commerce undir **Vefstillingar \> Viðbætur** er stilling gjafakortseiningar sem kallast **Studd gerð gjafakorts**.</span><span class="sxs-lookup"><span data-stu-id="fd801-127">In Commerce site builder under **Site Settings \> Extensions**, there is a gift card module setting called **Supported gift card type**.</span></span> <span data-ttu-id="fd801-128">Þessi stilling styður þrjú gildi:</span><span class="sxs-lookup"><span data-stu-id="fd801-128">This setting supports three values:</span></span>
- <span data-ttu-id="fd801-129">**Dynamics 365 gjafakort** - Þegar þessari stillingu er beitt leyfir gjafakortseiningin aðeins innlausn á Dynamics 365 gjafakortum.</span><span class="sxs-lookup"><span data-stu-id="fd801-129">**Dynamics 365 gift card** - When this setting is applied, the gift card module only allows the redemption of Dynamics 365 gift cards.</span></span> <span data-ttu-id="fd801-130">Þessi stilling er aðeins studd fyrir innskráða notendur á e-verslunarsíðunni.</span><span class="sxs-lookup"><span data-stu-id="fd801-130">This setting is only supported for signed-in users on the e-Commerce site.</span></span>
- <span data-ttu-id="fd801-131">**SVS og Givex gjafakort** - Þegar þessari stillingu er beitt leyfir gjafakortseiningin aðeins innlausn á Givex og SVS gjafakortum.</span><span class="sxs-lookup"><span data-stu-id="fd801-131">**SVS and Givex gift cards** - When this setting is applied, the gift card module only allows the redemption of Givex and SVS gift cards.</span></span> <span data-ttu-id="fd801-132">Þessi stilling er studd fyrir innskráða og nafnlausa notendur á e-verslunarsíðunni.</span><span class="sxs-lookup"><span data-stu-id="fd801-132">This setting is supported for signed-in and anonymous users on the e-Commerce site.</span></span>
- <span data-ttu-id="fd801-133">**Dynamics 365, SVS og Givex gjafakort** - Þegar þessari stillingu er beitt leyfir gjafakortseiningin aðeins innlausn á Dynamics 365, Givex og SVS gjafakortum.</span><span class="sxs-lookup"><span data-stu-id="fd801-133">**Dynamics 365, SVS, and Givex gift cards** - When this setting is applied, the gift card module allows the redemption of Dynamics 365, Givex, and SVS gift cards.</span></span> <span data-ttu-id="fd801-134">Þessi stilling er aðeins studd fyrir innskráða notendur á e-verslunarsíðunni.</span><span class="sxs-lookup"><span data-stu-id="fd801-134">This setting is only supported for signed-in users on the e-Commerce site.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="fd801-135">Þessar stillingar eru í boði í Dynamics 365 Commerce útgáfu 10.0.11 og eru aðeins nauðsynlegar ef stuðningur er fyrir SVS eða Givex-gjafakort.</span><span class="sxs-lookup"><span data-stu-id="fd801-135">These settings are available in the Dynamics 365 Commerce 10.0.11 release and are required only if you need support for SVS or Givex gift cards.</span></span> <span data-ttu-id="fd801-136">Ef verið er að uppfæra úr eldri útgáfu af Dynamics 365 Commerce verður að uppfæra appsettings.json-skrána handvirkt.</span><span class="sxs-lookup"><span data-stu-id="fd801-136">If you are updating from an older version of Dynamics 365 Commerce, you must manually update the appsettings.json file.</span></span> <span data-ttu-id="fd801-137">Leiðbeiningar um uppfærslu appsettings.json skrárinnar er að finna í [Uppfærslur á SDK og einingasafni](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span><span class="sxs-lookup"><span data-stu-id="fd801-137">For instructions on updating the appsettings.json file, see [SDK and module library updates](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span></span> 

## <a name="add-a-gift-card-module-to-a-page"></a><span data-ttu-id="fd801-138">Bæta gjafakortseiningu við síðu</span><span class="sxs-lookup"><span data-stu-id="fd801-138">Add a gift card module to a page</span></span>

<span data-ttu-id="fd801-139">Leiðbeiningar um hvernig bæta skuli gjafakortseiningu við greiðslusíðu og stilla nauðsynlega eiginleika er að finna í [Greiðsluferliseining](add-checkout-module.md).</span><span class="sxs-lookup"><span data-stu-id="fd801-139">For instructions on how to add a gift card module to a checkout page and set the required properties, see [Checkout module](add-checkout-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="fd801-140">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="fd801-140">Additional resources</span></span>

[<span data-ttu-id="fd801-141">Körfueining</span><span class="sxs-lookup"><span data-stu-id="fd801-141">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="fd801-142">Körfutáknseining</span><span class="sxs-lookup"><span data-stu-id="fd801-142">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="fd801-143">Greiðsluferliseining</span><span class="sxs-lookup"><span data-stu-id="fd801-143">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="fd801-144">Greiðslueining</span><span class="sxs-lookup"><span data-stu-id="fd801-144">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="fd801-145">Sendingaraðseturseining</span><span class="sxs-lookup"><span data-stu-id="fd801-145">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="fd801-146">Afhendingarkostaeining</span><span class="sxs-lookup"><span data-stu-id="fd801-146">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="fd801-147">Eining fyrir afhendingarupplýsingar</span><span class="sxs-lookup"><span data-stu-id="fd801-147">Pickup information module</span></span>](pickup-info-module.md)

[<span data-ttu-id="fd801-148">Pöntunarupplýsingaeining</span><span class="sxs-lookup"><span data-stu-id="fd801-148">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="fd801-149">Stuðningur við utanaðkomandi gjafakort</span><span class="sxs-lookup"><span data-stu-id="fd801-149">Support for external gift cards</span></span>](./dev-itpro/gift-card.md)

[<span data-ttu-id="fd801-150">Uppfærslur á SDK og kjarnasafni</span><span class="sxs-lookup"><span data-stu-id="fd801-150">SDK and module library updates</span></span>](e-commerce-extensibility/sdk-updates.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]