---
title: Gjafakortseining
description: Þetta efni fjallar um gjafakortseiningar og lýsir því hvernig á að bæta þeim við vefsíður hjá Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 04/29/2021
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
ms.openlocfilehash: 8db7e597241f1fd552f6b960c2b57b0ba83da949
ms.sourcegitcommit: efde05c758b2e02960760d875569d780d77d5550
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/29/2021
ms.locfileid: "5962764"
---
# <a name="gift-card-module"></a><span data-ttu-id="f4843-103">Gjafakortseining</span><span class="sxs-lookup"><span data-stu-id="f4843-103">Gift card module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="f4843-104">Þetta efni fjallar um gjafakortseiningar og lýsir því hvernig á að bæta þeim við vefsíður hjá Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="f4843-104">This topic covers gift card modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="f4843-105">Hægt er að nota einingar gjafakorta við greiðslueiningar til að taka á móti gjafakortum, sem er algeng gerð greiðsla sem eru notaðar fyrir rafræn viðskipti.</span><span class="sxs-lookup"><span data-stu-id="f4843-105">Gift card modules can be used in checkout modules to accept gift cards, a common form of payment used for e-Commerce transactions.</span></span> <span data-ttu-id="f4843-106">Gjafakortseiningin styður Dynamics 365, SVS og Givex gjafakort.</span><span class="sxs-lookup"><span data-stu-id="f4843-106">The gift card module supports Dynamics 365, SVS, and Givex gift cards.</span></span> <span data-ttu-id="f4843-107">Gjafakort SVS og Givex eru innleyst með Adyen greiðsluþjónustuaðila.</span><span class="sxs-lookup"><span data-stu-id="f4843-107">SVS and Givex gift cards are redeemed via the Adyen payment provider.</span></span> <span data-ttu-id="f4843-108">Frekari upplýsingar um stuðning við gjafakort, svo sem SVS og Givex, eru í [Stuðningur við utanaðkomandi gjafakort](./dev-itpro/gift-card.md).</span><span class="sxs-lookup"><span data-stu-id="f4843-108">For more information about support for external gift cards such as SVS and Givex, see [Support for external gift cards](./dev-itpro/gift-card.md).</span></span>

> [!NOTE]
> <span data-ttu-id="f4843-109">Stuðningur við innlausn SVS og Givex-gjafakorta við greiðsluferli er í boði í Dynamics 365 Commerce útgáfu 10.0.11.</span><span class="sxs-lookup"><span data-stu-id="f4843-109">Support for redeeming SVS and Givex gift cards during checkout flow is available in the Dynamics 365 Commerce 10.0.11 release.</span></span> 

<span data-ttu-id="f4843-110">Tvær gjafakortseiningar eru í boði:</span><span class="sxs-lookup"><span data-stu-id="f4843-110">There are two gift card modules available:</span></span>

- <span data-ttu-id="f4843-111">**Gjafakort** - Hægt er að nota þessa einingu á greiðslusíðu til að innleysa gjafakort sem tilboð.</span><span class="sxs-lookup"><span data-stu-id="f4843-111">**Gift card** – This module can be used on a checkout page to redeem a gift card as tender.</span></span> 
- <span data-ttu-id="f4843-112">**Könnun á stöðu gjafakorts** - Hægt er að nota þessa einingu á hvaða síðu sem er til að skoða stöðuna á gjafakorti.</span><span class="sxs-lookup"><span data-stu-id="f4843-112">**Gift card balance check** – This module can be used on any page to check the balance on a gift card.</span></span> <span data-ttu-id="f4843-113">Þessi eining er tiltæk í Commerce Release 10.0.14 og nýrri.</span><span class="sxs-lookup"><span data-stu-id="f4843-113">This module is available in Commerce release 10.0.14 and later.</span></span>

> [!NOTE]
> <span data-ttu-id="f4843-114">Stuðningur við fyrir athugunarstöðu gjafakorts er tiltækur í Dynamics 365 Commerce útgáfu 10.0.14.</span><span class="sxs-lookup"><span data-stu-id="f4843-114">Support for the gift card balance check module is available in the Dynamics 365 Commerce 10.0.14 release.</span></span>

<span data-ttu-id="f4843-115">Eftirfarandi mynd sýnir dæmi um gjafakortseiningu á greiðsluferlissíðu.</span><span class="sxs-lookup"><span data-stu-id="f4843-115">The following image shows an example of a gift card module on a checkout page.</span></span>

![Dæmi um gjafakortseiningu](./media/ecommerce-giftcard.PNG)

## <a name="module-properties"></a><span data-ttu-id="f4843-117">Eiginleikar einingar</span><span class="sxs-lookup"><span data-stu-id="f4843-117">Module properties</span></span>

- <span data-ttu-id="f4843-118">**Sýna fleiri reiti** - Þessi eiginleiki skilgreinir hvaða reiti skuli birta fyrir gjafakort auk gjafakortsnúmersins sem er alltaf birt sjálfgefið.</span><span class="sxs-lookup"><span data-stu-id="f4843-118">**Show additional fields** – This property defines what fields should be displayed for gift cards in addition to the gift card number, which is always displayed by default.</span></span> <span data-ttu-id="f4843-119">Til dæmis styðja sum gjafakort með birtinu á persónuauðkenni (PIN) og önnur styðja birtingu PIN og gildistíma.</span><span class="sxs-lookup"><span data-stu-id="f4843-119">For example, some gift cards support displaying a personal identification number (PIN), and others support displaying a PIN and expiration date.</span></span> <span data-ttu-id="f4843-120">Að öðrum kosti væri hægt að stilla þennan eiginleika á „Enginn“, sem myndi aðeins sýna gjafakortsnúmerið og enga viðbótarreiti.</span><span class="sxs-lookup"><span data-stu-id="f4843-120">Alternatively, this property could be set to "None", which would only display the gift card number and no additional fields.</span></span>

<span data-ttu-id="f4843-121">Studd gildi:</span><span class="sxs-lookup"><span data-stu-id="f4843-121">Supported values:</span></span>
-   <span data-ttu-id="f4843-122">PIN</span><span class="sxs-lookup"><span data-stu-id="f4843-122">PIN</span></span>
-   <span data-ttu-id="f4843-123">Gildistími</span><span class="sxs-lookup"><span data-stu-id="f4843-123">Expiration date</span></span>
-   <span data-ttu-id="f4843-124">PIN og lokadagur</span><span class="sxs-lookup"><span data-stu-id="f4843-124">PIN and expiration date</span></span> 
-   <span data-ttu-id="f4843-125">None</span><span class="sxs-lookup"><span data-stu-id="f4843-125">None</span></span>

## <a name="site-settings-for-gift-card-modules"></a><span data-ttu-id="f4843-126">Vefstillingar fyrir gjafakortseiningar</span><span class="sxs-lookup"><span data-stu-id="f4843-126">Site settings for gift card modules</span></span>

<span data-ttu-id="f4843-127">Í vefsvæðishönnuði Commerce undir **Vefstillingar \> Viðbætur** er stilling gjafakortseiningar sem kallast **Studd gerð gjafakorts**.</span><span class="sxs-lookup"><span data-stu-id="f4843-127">In Commerce site builder under **Site Settings \> Extensions**, there is a gift card module setting called **Supported gift card type**.</span></span> <span data-ttu-id="f4843-128">Þessi stilling styður þrjú gildi:</span><span class="sxs-lookup"><span data-stu-id="f4843-128">This setting supports three values:</span></span>
- <span data-ttu-id="f4843-129">**Dynamics 365 gjafakort** - Þegar þessari stillingu er beitt leyfir gjafakortseiningin aðeins innlausn á Dynamics 365 gjafakortum.</span><span class="sxs-lookup"><span data-stu-id="f4843-129">**Dynamics 365 gift card** – When this setting is applied, the gift card module only allows the redemption of Dynamics 365 gift cards.</span></span> <span data-ttu-id="f4843-130">Þessi stilling er aðeins studd fyrir innskráða notendur á e-verslunarsíðunni.</span><span class="sxs-lookup"><span data-stu-id="f4843-130">This setting is only supported for signed-in users on the e-Commerce site.</span></span>
- <span data-ttu-id="f4843-131">**SVS og Givex gjafakort** - Þegar þessari stillingu er beitt leyfir gjafakortseiningin aðeins innlausn á Givex og SVS gjafakortum.</span><span class="sxs-lookup"><span data-stu-id="f4843-131">**SVS and Givex gift cards** – When this setting is applied, the gift card module only allows the redemption of Givex and SVS gift cards.</span></span> <span data-ttu-id="f4843-132">Þessi stilling er studd fyrir innskráða og nafnlausa notendur á e-verslunarsíðunni.</span><span class="sxs-lookup"><span data-stu-id="f4843-132">This setting is supported for signed-in and anonymous users on the e-Commerce site.</span></span>
- <span data-ttu-id="f4843-133">**Dynamics 365, SVS og Givex gjafakort** - Þegar þessari stillingu er beitt leyfir gjafakortseiningin aðeins innlausn á Dynamics 365, Givex og SVS gjafakortum.</span><span class="sxs-lookup"><span data-stu-id="f4843-133">**Dynamics 365, SVS, and Givex gift cards** – When this setting is applied, the gift card module allows the redemption of Dynamics 365, Givex, and SVS gift cards.</span></span> <span data-ttu-id="f4843-134">Þessi stilling er aðeins studd fyrir innskráða notendur á e-verslunarsíðunni.</span><span class="sxs-lookup"><span data-stu-id="f4843-134">This setting is only supported for signed-in users on the e-Commerce site.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f4843-135">Þessar stillingar eru í boði í Dynamics 365 Commerce útgáfu 10.0.11 og eru aðeins nauðsynlegar ef stuðningur er fyrir SVS eða Givex-gjafakort.</span><span class="sxs-lookup"><span data-stu-id="f4843-135">These settings are available in the Dynamics 365 Commerce 10.0.11 release and are required only if you need support for SVS or Givex gift cards.</span></span> <span data-ttu-id="f4843-136">Ef verið er að uppfæra úr eldri útgáfu af Dynamics 365 Commerce verður að uppfæra appsettings.json-skrána handvirkt.</span><span class="sxs-lookup"><span data-stu-id="f4843-136">If you are updating from an older version of Dynamics 365 Commerce, you must manually update the appsettings.json file.</span></span> <span data-ttu-id="f4843-137">Leiðbeiningar um uppfærslu appsettings.json skrárinnar er að finna í [Uppfærslur á SDK og einingasafni](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span><span class="sxs-lookup"><span data-stu-id="f4843-137">For instructions on updating the appsettings.json file, see [SDK and module library updates](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span></span> 

## <a name="extend-internal-gift-cards-for-use-in-e-commerce-storefronts"></a><span data-ttu-id="f4843-138">Útvíkka notkun innri gjafakorta til að nota í netverslun rafrænna viðskipta</span><span class="sxs-lookup"><span data-stu-id="f4843-138">Extend internal gift cards for use in e-commerce storefronts</span></span>

<span data-ttu-id="f4843-139">Innri gjafakort eru sjálfgefið ekki stillt inn á notkun í netverslunum rafrænna viðskipta.</span><span class="sxs-lookup"><span data-stu-id="f4843-139">By default, internal gift cards aren't optimized for use in e-commerce storefronts.</span></span> <span data-ttu-id="f4843-140">Áður en leyft er að nota innri gjafakort fyrir greiðslu ætti því að stilla þau með viðbótum sem stuðla að því að gera þau öruggari.</span><span class="sxs-lookup"><span data-stu-id="f4843-140">Therefore, before you allow internal gift cards to be used for payment, you should configure them with extensions that help make them more secure.</span></span> <span data-ttu-id="f4843-141">Hér eru gjafakortasvæðin sem ætti að víkka út áður en leyfa á notkun innri gjafakorta í framleiðslu:</span><span class="sxs-lookup"><span data-stu-id="f4843-141">Here are the gift card areas that you should extend before you allow internal gift cards to be used in production:</span></span>

- <span data-ttu-id="f4843-142">**Gjafakortsnúmer** – Númeraraðir er notaðar til að mynda gjafakortsnúmer fyrir innri gjafakort.</span><span class="sxs-lookup"><span data-stu-id="f4843-142">**Gift card number** – Number sequences are used to generate gift card numbers for internal gift cards.</span></span> <span data-ttu-id="f4843-143">Þar sem auðvelt er að spá fyrir um númeraraðir ættir þú að víkka út myndun á gjafakortanúmerum þannig að handahófskenndir, dulkóðaðir strengir séu notaðir fyrir gjafakortanúmer sem gefin eru út.</span><span class="sxs-lookup"><span data-stu-id="f4843-143">Because number sequences can easily be predicted, you should extend the generation of gift card numbers so that random, cryptographically secure strings are used for the gift card numbers that are issued.</span></span>
- <span data-ttu-id="f4843-144">**GetBalance** – **GetBalance** API er notað til að fletta upp á innistæðum gjafakorta.</span><span class="sxs-lookup"><span data-stu-id="f4843-144">**GetBalance** – The **GetBalance** API is used to look up gift card balances.</span></span> <span data-ttu-id="f4843-145">Þetta API er opinbert að sjálfgefnu.</span><span class="sxs-lookup"><span data-stu-id="f4843-145">By default, this API public.</span></span> <span data-ttu-id="f4843-146">Ef ekki er krafist PIN-númers til að fletta upp á innistæðum gjafakorta er hætt á að kerfisbundnar árásir noti **GetBalance** API í tilraun til að fletta upp á gjafakortanúmerum sem eru með innstæður.</span><span class="sxs-lookup"><span data-stu-id="f4843-146">If a PIN isn't required to look up gift card balances, there is a risk that brute force attacks could use the **GetBalance** API to try to look up gift card numbers that have balances.</span></span> <span data-ttu-id="f4843-147">Með því að innleiða bæði kröfur um PIN-númer fyrir innri gjafakort og API-takmörkun geturðu stuðlað að því að draga úr áhættunni.</span><span class="sxs-lookup"><span data-stu-id="f4843-147">By implementing both PIN requirements for internal gift cards and API throttling, you can help mitigate the risk.</span></span>
- <span data-ttu-id="f4843-148">**PIN** – Innri gjafakort styðja ekki PIN-númer.</span><span class="sxs-lookup"><span data-stu-id="f4843-148">**PIN** – By default, internal gift cards don't support PINs.</span></span> <span data-ttu-id="f4843-149">Þú ættir að framlengja innri gjafakort þannig að það þarf PIN-númer til að fletta upp stöðu.</span><span class="sxs-lookup"><span data-stu-id="f4843-149">You should extend internal gift cards so that a PIN is required to look up balances.</span></span> <span data-ttu-id="f4843-150">Þessa virkni er einnig hægt að nota til að læsa gjafakortum eftir nokkrar rangar tilraunir í röð við að slá inn PIN-númer.</span><span class="sxs-lookup"><span data-stu-id="f4843-150">This functionality can also be used to lock gift cards after consecutive incorrect attempts to enter the PIN.</span></span>

## <a name="enable-gift-card-payments-for-guest-checkout"></a><span data-ttu-id="f4843-151">Virkja gjafakortagreiðslur fyrir greiðsluferli gests</span><span class="sxs-lookup"><span data-stu-id="f4843-151">Enable gift card payments for guest checkout</span></span>

<span data-ttu-id="f4843-152">Sjálfgefið er að gjafakortsgreiðslur séu ekki virkar fyrir (nafnlausar) greiðslur gesta.</span><span class="sxs-lookup"><span data-stu-id="f4843-152">By default, gift card payments aren't enabled for guest (anonymous) checkout.</span></span> <span data-ttu-id="f4843-153">Til að virkja þetta skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="f4843-153">To enable them, follow these steps.</span></span>

1. <span data-ttu-id="f4843-154">Í Commerce Headquarters skal fara í **Retail og Commerce \> Uppsetningu rásar \> Uppsetning POS \> POS \> POS-aðgerðir**.</span><span class="sxs-lookup"><span data-stu-id="f4843-154">In Commerce headquarters, go to **Retail and Commerce \> Channel setup \> POS setup \> POS \> POS Operations**.</span></span>
1. <span data-ttu-id="f4843-155">Veljið og haldið (eða hægrismellið) á haus netsins og veljið svo **Setja inn dálka**.</span><span class="sxs-lookup"><span data-stu-id="f4843-155">Select and hold (or right-click) the header of the grid, and then select **Insert columns**.</span></span>
1. <span data-ttu-id="f4843-156">Í svarglugganum **Setja inn dálka** skal velja gátreitinn **AllowAnonymousAccess**.</span><span class="sxs-lookup"><span data-stu-id="f4843-156">In the **Insert columns** dialog box, select the **AllowAnonymousAccess** check box.</span></span>
1. <span data-ttu-id="f4843-157">Veldu **Uppfæra**.</span><span class="sxs-lookup"><span data-stu-id="f4843-157">Select **Update**.</span></span>
1. <span data-ttu-id="f4843-158">Fyrir aðgerðir **520** (innistæða gjafakorts) og **214** skal stilla gildið **AllowAnonymousAccess** á **1**.</span><span class="sxs-lookup"><span data-stu-id="f4843-158">For operations **520** (Gift card balance) and **214**, set the **AllowAnonymousAccess** value to **1**.</span></span>
1. <span data-ttu-id="f4843-159">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="f4843-159">Select **Save**.</span></span>
1. <span data-ttu-id="f4843-160">Keyrið verkraðara **1090** til að samstilla breytingar við gagnagrunn rásarinnar.</span><span class="sxs-lookup"><span data-stu-id="f4843-160">Run the **1090** scheduler job to sync changes to the channel database.</span></span> 

## <a name="add-a-gift-card-module-to-a-page"></a><span data-ttu-id="f4843-161">Bæta gjafakortseiningu við síðu</span><span class="sxs-lookup"><span data-stu-id="f4843-161">Add a gift card module to a page</span></span>

<span data-ttu-id="f4843-162">Leiðbeiningar um hvernig bæta skuli gjafakortseiningu við greiðslusíðu og stilla nauðsynlega eiginleika er að finna í [Greiðsluferliseining](add-checkout-module.md).</span><span class="sxs-lookup"><span data-stu-id="f4843-162">For instructions on how to add a gift card module to a checkout page and set the required properties, see [Checkout module](add-checkout-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f4843-163">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="f4843-163">Additional resources</span></span>

[<span data-ttu-id="f4843-164">Körfueining</span><span class="sxs-lookup"><span data-stu-id="f4843-164">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="f4843-165">Körfutáknseining</span><span class="sxs-lookup"><span data-stu-id="f4843-165">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="f4843-166">Greiðsluferliseining</span><span class="sxs-lookup"><span data-stu-id="f4843-166">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="f4843-167">Greiðslueining</span><span class="sxs-lookup"><span data-stu-id="f4843-167">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="f4843-168">Sendingaraðseturseining</span><span class="sxs-lookup"><span data-stu-id="f4843-168">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="f4843-169">Afhendingarkostaeining</span><span class="sxs-lookup"><span data-stu-id="f4843-169">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="f4843-170">Eining fyrir afhendingarupplýsingar</span><span class="sxs-lookup"><span data-stu-id="f4843-170">Pickup information module</span></span>](pickup-info-module.md)

[<span data-ttu-id="f4843-171">Pöntunarupplýsingaeining</span><span class="sxs-lookup"><span data-stu-id="f4843-171">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="f4843-172">Stuðningur við utanaðkomandi gjafakort</span><span class="sxs-lookup"><span data-stu-id="f4843-172">Support for external gift cards</span></span>](./dev-itpro/gift-card.md)

[<span data-ttu-id="f4843-173">Uppfærslur á SDK og kjarnasafni</span><span class="sxs-lookup"><span data-stu-id="f4843-173">SDK and module library updates</span></span>](e-commerce-extensibility/sdk-updates.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
