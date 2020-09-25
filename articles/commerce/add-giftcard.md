---
title: Gjafakortseining
description: Þetta efni fjallar um gjafakortseiningar og lýsir því hvernig á að bæta þeim við vefsíður hjá Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 08/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 4cc947b9d6f3cfa51bce2155170c49e9529d0f7d
ms.sourcegitcommit: 420b9e538f706178f8e1f2786e02f4f400bf2336
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/02/2020
ms.locfileid: "3761082"
---
# <a name="gift-card-module"></a><span data-ttu-id="f3ee4-103">Gjafakortseining</span><span class="sxs-lookup"><span data-stu-id="f3ee4-103">Gift card module</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="f3ee4-104">Þetta efni fjallar um gjafakortseiningar og lýsir því hvernig á að bæta þeim við vefsíður hjá Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="f3ee4-104">This topic covers gift card modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="f3ee4-105">Yfirlit</span><span class="sxs-lookup"><span data-stu-id="f3ee4-105">Overview</span></span>

<span data-ttu-id="f3ee4-106">Hægt er að nota einingar gjafakorta við greiðslueiningar til að taka á móti gjafakortum, sem er algeng gerð greiðsla sem eru notaðar fyrir rafræn viðskipti.</span><span class="sxs-lookup"><span data-stu-id="f3ee4-106">Gift card modules can be used in checkout modules to accept gift cards, a common form of payment used for e-Commerce transactions.</span></span> <span data-ttu-id="f3ee4-107">Gjafakortseiningin styður Dynamics 365, SVS og Givex gjafakort.</span><span class="sxs-lookup"><span data-stu-id="f3ee4-107">The gift card module supports Dynamics 365, SVS, and Givex gift cards.</span></span> <span data-ttu-id="f3ee4-108">Gjafakort SVS og Givex eru innleyst með Adyen greiðsluþjónustuaðila.</span><span class="sxs-lookup"><span data-stu-id="f3ee4-108">SVS and Givex gift cards are redeemed via the Adyen payment provider.</span></span> <span data-ttu-id="f3ee4-109">Frekari upplýsingar um stuðning við gjafakort, svo sem SVS og Givex, eru í [Stuðningur við utanaðkomandi gjafakort](./dev-itpro/gift-card.md).</span><span class="sxs-lookup"><span data-stu-id="f3ee4-109">For more information about support for external gift cards such as SVS and Givex, see [Support for external gift cards](./dev-itpro/gift-card.md).</span></span>

<span data-ttu-id="f3ee4-110">Tvær gjafakortseiningar eru í boði:</span><span class="sxs-lookup"><span data-stu-id="f3ee4-110">There are two gift card modules available:</span></span>

- <span data-ttu-id="f3ee4-111">**Gjafakort** - Hægt er að nota þessa einingu á greiðslusíðu til að innleysa gjafakort sem tilboð.</span><span class="sxs-lookup"><span data-stu-id="f3ee4-111">**Gift card** - This module can be used on a checkout page to redeem a gift card as tender.</span></span> 
- <span data-ttu-id="f3ee4-112">**Könnun á stöðu gjafakorts** - Hægt er að nota þessa einingu á hvaða síðu sem er til að skoða stöðuna á gjafakorti.</span><span class="sxs-lookup"><span data-stu-id="f3ee4-112">**Gift card balance check** - This module can be used on any page to check the balance on a gift card.</span></span> <span data-ttu-id="f3ee4-113">Þessi eining er tiltæk í Commerce Release 10.0.14 og nýrri.</span><span class="sxs-lookup"><span data-stu-id="f3ee4-113">This module is available in Commerce release 10.0.14 and later.</span></span>

<span data-ttu-id="f3ee4-114">Eftirfarandi mynd sýnir dæmi um gjafakortseiningu á greiðsluferlissíðu.</span><span class="sxs-lookup"><span data-stu-id="f3ee4-114">The following image shows an example of a gift card module on a checkout page.</span></span>

![Dæmi um gjafakortseiningu](./media/ecommerce-giftcard.PNG)

## <a name="module-properties"></a><span data-ttu-id="f3ee4-116">Eiginleikar einingar</span><span class="sxs-lookup"><span data-stu-id="f3ee4-116">Module properties</span></span>

- <span data-ttu-id="f3ee4-117">**Sýna fleiri reiti** - Þessi eiginleiki skilgreinir hvaða reiti skuli birta fyrir gjafakort auk gjafakortsnúmersins sem er alltaf birt sjálfgefið.</span><span class="sxs-lookup"><span data-stu-id="f3ee4-117">**Show additional fields** - This property defines what fields should be displayed for gift cards in addition to the gift card number, which is always displayed by default.</span></span> <span data-ttu-id="f3ee4-118">Til dæmis styðja sum gjafakort með birtinu á persónuauðkenni (PIN) og önnur styðja birtingu PIN og gildistíma.</span><span class="sxs-lookup"><span data-stu-id="f3ee4-118">For example, some gift cards support displaying a personal identification number (PIN), and others support displaying a PIN and expiration date.</span></span> <span data-ttu-id="f3ee4-119">Að öðrum kosti væri hægt að stilla þennan eiginleika á „Enginn“, sem myndi aðeins sýna gjafakortsnúmerið og enga viðbótarreiti.</span><span class="sxs-lookup"><span data-stu-id="f3ee4-119">Alternatively, this property could be set to "None", which would only display the gift card number and no additional fields.</span></span>

<span data-ttu-id="f3ee4-120">Studd gildi:</span><span class="sxs-lookup"><span data-stu-id="f3ee4-120">Supported values:</span></span>
-   <span data-ttu-id="f3ee4-121">PIN</span><span class="sxs-lookup"><span data-stu-id="f3ee4-121">PIN</span></span>
-   <span data-ttu-id="f3ee4-122">Gildistími</span><span class="sxs-lookup"><span data-stu-id="f3ee4-122">Expiration date</span></span>
-   <span data-ttu-id="f3ee4-123">PIN og lokadagur</span><span class="sxs-lookup"><span data-stu-id="f3ee4-123">PIN and expiration date</span></span> 
-   <span data-ttu-id="f3ee4-124">None</span><span class="sxs-lookup"><span data-stu-id="f3ee4-124">None</span></span>

## <a name="site-settings-for-gift-card-modules"></a><span data-ttu-id="f3ee4-125">Vefstillingar fyrir gjafakortseiningar</span><span class="sxs-lookup"><span data-stu-id="f3ee4-125">Site settings for gift card modules</span></span>

<span data-ttu-id="f3ee4-126">Í vefsvæðishönnuði Commerce undir **Vefstillingar \> Viðbætur** er stilling gjafakortseiningar sem kallast **Studd gerð gjafakorts**.</span><span class="sxs-lookup"><span data-stu-id="f3ee4-126">In Commerce site builder under **Site Settings \> Extensions**, there is a gift card module setting called **Supported gift card type**.</span></span> <span data-ttu-id="f3ee4-127">Þessi stilling styður þrjú gildi:</span><span class="sxs-lookup"><span data-stu-id="f3ee4-127">This setting supports three values:</span></span>
- <span data-ttu-id="f3ee4-128">**Dynamics 365 gjafakort** - Þegar þessari stillingu er beitt leyfir gjafakortseiningin aðeins innlausn á Dynamics 365 gjafakortum.</span><span class="sxs-lookup"><span data-stu-id="f3ee4-128">**Dynamics 365 gift card** - When this setting is applied, the gift card module only allows the redemption of Dynamics 365 gift cards.</span></span> <span data-ttu-id="f3ee4-129">Þessi stilling er aðeins studd fyrir innskráða notendur á e-verslunarsíðunni.</span><span class="sxs-lookup"><span data-stu-id="f3ee4-129">This setting is only supported for signed-in users on the e-Commerce site.</span></span>
- <span data-ttu-id="f3ee4-130">**SVS og Givex gjafakort** - Þegar þessari stillingu er beitt leyfir gjafakortseiningin aðeins innlausn á Givex og SVS gjafakortum.</span><span class="sxs-lookup"><span data-stu-id="f3ee4-130">**SVS and Givex gift cards** - When this setting is applied, the gift card module only allows the redemption of Givex and SVS gift cards.</span></span> <span data-ttu-id="f3ee4-131">Þessi stilling er studd fyrir innskráða og nafnlausa notendur á e-verslunarsíðunni.</span><span class="sxs-lookup"><span data-stu-id="f3ee4-131">This setting is supported for signed-in and anonymous users on the e-Commerce site.</span></span>
- <span data-ttu-id="f3ee4-132">**Dynamics 365, SVS og Givex gjafakort** - Þegar þessari stillingu er beitt leyfir gjafakortseiningin aðeins innlausn á Dynamics 365, Givex og SVS gjafakortum.</span><span class="sxs-lookup"><span data-stu-id="f3ee4-132">**Dynamics 365, SVS, and Givex gift cards** - When this setting is applied, the gift card module allows the redemption of Dynamics 365, Givex, and SVS gift cards.</span></span> <span data-ttu-id="f3ee4-133">Þessi stilling er aðeins studd fyrir innskráða notendur á e-verslunarsíðunni.</span><span class="sxs-lookup"><span data-stu-id="f3ee4-133">This setting is only supported for signed-in users on the e-Commerce site.</span></span>

## <a name="add-a-gift-card-module-to-a-page"></a><span data-ttu-id="f3ee4-134">Bæta gjafakortseiningu við síðu</span><span class="sxs-lookup"><span data-stu-id="f3ee4-134">Add a gift card module to a page</span></span>

<span data-ttu-id="f3ee4-135">Leiðbeiningar um hvernig bæta skuli gjafakortseiningu við greiðslusíðu og stilla nauðsynlega eiginleika er að finna í [Greiðsluferliseining](add-checkout-module.md).</span><span class="sxs-lookup"><span data-stu-id="f3ee4-135">For instructions on how to add a gift card module to a checkout page and set the required properties, see [Checkout module](add-checkout-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f3ee4-136">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="f3ee4-136">Additional resources</span></span>

[<span data-ttu-id="f3ee4-137">Körfueining</span><span class="sxs-lookup"><span data-stu-id="f3ee4-137">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="f3ee4-138">Körfutáknseining</span><span class="sxs-lookup"><span data-stu-id="f3ee4-138">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="f3ee4-139">Greiðsluferliseining</span><span class="sxs-lookup"><span data-stu-id="f3ee4-139">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="f3ee4-140">Greiðslueining</span><span class="sxs-lookup"><span data-stu-id="f3ee4-140">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="f3ee4-141">Eining sendingaraðseturs</span><span class="sxs-lookup"><span data-stu-id="f3ee4-141">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="f3ee4-142">Eining afhendingarvalkosta</span><span class="sxs-lookup"><span data-stu-id="f3ee4-142">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="f3ee4-143">Pöntunarupplýsingaeining</span><span class="sxs-lookup"><span data-stu-id="f3ee4-143">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="f3ee4-144">Stuðningur við utanaðkomandi gjafakort</span><span class="sxs-lookup"><span data-stu-id="f3ee4-144">Support for external gift cards</span></span>](./dev-itpro/gift-card.md)
