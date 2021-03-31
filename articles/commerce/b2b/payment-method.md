---
title: Skilgreina greiðslumáta viðskiptavinalykils fyrir B2B-svæði fyrir rafræn viðskipti
description: Þetta efnisatriði lýsir því hvernig á að skilgreina greiðslumáta viðskiptavinalykils fyrir B2B-svæði rafrænna viðskipta.
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
ms.openlocfilehash: 82dfd6ac7e97d838ef442fd6ded4a4f165fc795b
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5211202"
---
# <a name="configure-the-customer-account-payment-method-for-b2b-e-commerce-sites"></a><span data-ttu-id="d5b97-103">Skilgreina greiðslumáta viðskiptavinalykils fyrir B2B-svæði fyrir rafræn viðskipti</span><span class="sxs-lookup"><span data-stu-id="d5b97-103">Configure the customer account payment method for B2B e-commerce sites</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d5b97-104">Þetta efnisatriði lýsir því hvernig á að skilgreina greiðslumáta viðskiptavinalykils fyrir B2B-svæði rafrænna viðskipta.</span><span class="sxs-lookup"><span data-stu-id="d5b97-104">This topic describes how to configure the customer account payment method for business-to-business (B2B) e-commerce sites.</span></span>

<span data-ttu-id="d5b97-105">Smásalar geta tekið við ýmsum gerðum af greiðslum í staðinn fyrir afurðir og þjónustu sem þeir selja í rás rafrænna viðskipta.</span><span class="sxs-lookup"><span data-stu-id="d5b97-105">Retailers can accept various types of payment in exchange for the products and services that they sell in an e-commerce channel.</span></span> <span data-ttu-id="d5b97-106">Hver greiðslugerð sem smásali samþykkir verður að vera skilgreind í Microsoft Dynamics 365 Commerce þegar kerfið er sett upp.</span><span class="sxs-lookup"><span data-stu-id="d5b97-106">Each payment type that a retailer accepts must be configured in Microsoft Dynamics 365 Commerce when the system is set up.</span></span> <span data-ttu-id="d5b97-107">Greiðslumáti viðskiptavinalykils (eða „á lykli“) verður að vera studdur á B2B-svæðum rafrænna viðskipta.</span><span class="sxs-lookup"><span data-stu-id="d5b97-107">The customer account (or "on account") payment method must be supported on B2B e-commerce sites.</span></span> 

## <a name="prerequisites"></a><span data-ttu-id="d5b97-108">Forkröfur</span><span class="sxs-lookup"><span data-stu-id="d5b97-108">Prerequisites</span></span>

1. <span data-ttu-id="d5b97-109">Bætið greiðslumáta viðskiptavinalykils við Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="d5b97-109">Add the customer account payment method in Commerce headquarters.</span></span>
2. <span data-ttu-id="d5b97-110">Tengið greiðslumáta viðskiptavinalykils við rás rafrænna viðskipta.</span><span class="sxs-lookup"><span data-stu-id="d5b97-110">Associate the customer account payment method with the e-commerce channel.</span></span>
3. <span data-ttu-id="d5b97-111">Gangið úr skugga um að **Leyfa á lykli** sé virkjað fyrir viðskiptavininn í **Smásala og viðskipti \> Viðskiptavinir \> Allir viðskiptavinir \> Sjálfgildi greiðslu** í Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="d5b97-111">Make sure that **Allow on account** is enabled for the customer at **Retail and Commerce \> Customers \> All customers \> Payment defaults** in Commerce headquarters.</span></span> <span data-ttu-id="d5b97-112">Gangið einnig úr skugga um að færibreytur **Lánamarks** séu rétt stilltar fyrir viðskiptavininn í **Smásala og viðskipti \> Viðskiptavinir \> Allir viðskiptavinir \> Skuldir og innheimta** í Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="d5b97-112">Also make sure that **Credit limit** parameters are set appropriately for the customer at **Retail and Commerce \> Customers \> All customers \> Credit and Collections** in Commerce headquarters.</span></span> 

## <a name="enable-the-customer-account-payment-method-in-commerce-site-builder"></a><span data-ttu-id="d5b97-113">Virkja greiðslumáta fyrir viðskiptavinalykil í Commerce Site Builder</span><span class="sxs-lookup"><span data-stu-id="d5b97-113">Enable the customer account payment method in Commerce site builder</span></span> 

<span data-ttu-id="d5b97-114">Til að virkja greiðslumáta fyrir viðskiptavinalykil í Commerce Site Builder skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="d5b97-114">To enable the customer account payment method in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="d5b97-115">Farið í **Svæðisstillingar \> Viðbætur**.</span><span class="sxs-lookup"><span data-stu-id="d5b97-115">Go to **Site Settings \> Extensions**.</span></span>
1. <span data-ttu-id="d5b97-116">Stillið eiginleikann **Virkja greiðslur viðskiptavinalykils** á **Virkjað fyrir B2B-viðskiptavini**.</span><span class="sxs-lookup"><span data-stu-id="d5b97-116">Set the **Enable customer account payments** property to **Enabled for B2B customers**.</span></span> 
1. <span data-ttu-id="d5b97-117">Veldur **Vista og birta**.</span><span class="sxs-lookup"><span data-stu-id="d5b97-117">Select **Save and Publish**.</span></span>

> [!NOTE]
> <span data-ttu-id="d5b97-118">Nýjar svæðisstillingar taka gildi aðeins eftir að búið er að uppfæra skrána app.settings.json.</span><span class="sxs-lookup"><span data-stu-id="d5b97-118">The new site settings take effect only after the app.settings.json file is updated.</span></span> <span data-ttu-id="d5b97-119">Frekari upplýsingar er að finna í [Uppfærslur á SDK og einingasafni](../e-commerce-extensibility/sdk-updates.md).</span><span class="sxs-lookup"><span data-stu-id="d5b97-119">For more information, see [SDK and Module library updates](../e-commerce-extensibility/sdk-updates.md).</span></span>

## <a name="enable-the-customer-account-payment-method-on-the-checkout-page-for-the-b2b-e-commerce-site"></a><span data-ttu-id="d5b97-120">Virkja greiðslumáta fyrir viðskiptavinalykil á greiðslusíðu fyrir B2B-svæði rafrænna viðskipta</span><span class="sxs-lookup"><span data-stu-id="d5b97-120">Enable the customer account payment method on the checkout page for the B2B e-commerce site</span></span>

<span data-ttu-id="d5b97-121">Til að virkja greiðslumáta viðskiptavinalykils á greiðslusíðunni fyrir B2B-svæði rafrænna viðskipta skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="d5b97-121">To enable the customer account payment method on the checkout page for the B2B e-commerce site, follow these steps.</span></span>

1. <span data-ttu-id="d5b97-122">Í Commerce Site Builder skal finna og breyta greiðslusíðunni eða brotinu sem inniheldur greiðslueininguna fyrir B2B-svæði rafrænna viðskipta.</span><span class="sxs-lookup"><span data-stu-id="d5b97-122">In Commerce site builder, find and edit the checkout page or fragment that contains the checkout module for the B2B e-commerce site.</span></span>
1. <span data-ttu-id="d5b97-123">Í raufinni **Hólf greiðsluferlishluta** skal velja **Bæta við einingu** og síðan bæta við einingu **Greiðsla með viðskiptavinalykli**.</span><span class="sxs-lookup"><span data-stu-id="d5b97-123">In the **Checkout section container** slot, select **Add Module**, and then add a **Customer account payment** module.</span></span>
1. <span data-ttu-id="d5b97-124">Staðsetjið eininguna **Greiðsla með viðskiptavinalykli** með því að velja úrfellingarmerkið (**...**) og veljið síðan **Færa upp** eða **Færa niður** eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="d5b97-124">Position the **Customer account payment** module by selecting the ellipsis (**...**), and then selecting **Move Up** or **Move Down** as required.</span></span>
1. <span data-ttu-id="d5b97-125">Veldu **Vista**, síðan **Ljúka við breytingar** til að skila síðunni og veldu síðan **Birta** til að birta hana.</span><span class="sxs-lookup"><span data-stu-id="d5b97-125">Select **Save**, select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="confirm-that-the-customer-account-payment-method-has-been-enabled-and-published"></a><span data-ttu-id="d5b97-126">Staðfesta að greiðslumáti viðskiptavinalykils hafi verið virkjaður og gefin út</span><span class="sxs-lookup"><span data-stu-id="d5b97-126">Confirm that the customer account payment method has been enabled and published</span></span>

<span data-ttu-id="d5b97-127">Til að staðfesta að greiðslumáti viðskiptavinalykils hafi verið gerður virkur skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="d5b97-127">To confirm that the customer account payment method has been enabled, follow these steps.</span></span>

1. <span data-ttu-id="d5b97-128">Skráðu þig inn á svæði rafrænna viðskipta.</span><span class="sxs-lookup"><span data-stu-id="d5b97-128">Sign in to the e-commerce site.</span></span>
1. <span data-ttu-id="d5b97-129">Bætið afurð við körfuna.</span><span class="sxs-lookup"><span data-stu-id="d5b97-129">Add a product to the cart.</span></span>
1. <span data-ttu-id="d5b97-130">Farið á síðu greiðsluferlis.</span><span class="sxs-lookup"><span data-stu-id="d5b97-130">Go to the checkout page.</span></span> <span data-ttu-id="d5b97-131">Þar ætti að sjást nýi greiðslumáti **Viðskiptavinalykils**.</span><span class="sxs-lookup"><span data-stu-id="d5b97-131">You should see the new **Customer Account** payment method.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d5b97-132">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="d5b97-132">Additional resources</span></span>

[<span data-ttu-id="d5b97-133">Setja upp B2B-svæði fyrir rafræn viðskipti</span><span class="sxs-lookup"><span data-stu-id="d5b97-133">Set up a B2B e-commerce site</span></span>](set-up-b2b-site.md)

[<span data-ttu-id="d5b97-134">Stofna líkanastigveldi fyrir B2B-fyrirtæki</span><span class="sxs-lookup"><span data-stu-id="d5b97-134">Create org modeling hierarchies for B2B organizations</span></span>](org-model.md)

[<span data-ttu-id="d5b97-135">Stjórna notendum viðskiptafélaga á B2B-svæði fyrir rafræn viðskipti</span><span class="sxs-lookup"><span data-stu-id="d5b97-135">Manage business partner users on B2B e-commerce sites</span></span>](manage-b2b-users.md)

[<span data-ttu-id="d5b97-136">Stilla takmörk afurðarmagns fyrir rafræn B2B-vefsvæði</span><span class="sxs-lookup"><span data-stu-id="d5b97-136">Set product quantity limits for B2B e-commerce sites</span></span>](quantity-limits.md)

[<span data-ttu-id="d5b97-137">Uppfærslur á SDK og kjarnasafni</span><span class="sxs-lookup"><span data-stu-id="d5b97-137">SDK and Module library updates</span></span>](../e-commerce-extensibility/sdk-updates.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]