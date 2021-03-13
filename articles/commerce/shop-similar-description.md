---
title: Virkja ráðleggingar um „versla svipaða lýsingu“
description: Þetta efnisatriði lýsir því hvernig á að virkja vörutillögurnar fyrir „versla vörur með svipaðri lýsingu“ í Microsoft Dynamics 365 Commerce.
author: bsokolov
manager: AnnBe
ms.date: 01/13/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: b3b7abf47a3bdacaa4b91ae32b68a809a84b0b1d
ms.sourcegitcommit: 872600103d2a444d78963867e5e0cdc62e68c3ec
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/01/2021
ms.locfileid: "5098632"
---
# <a name="enable-shop-similar-description-recommendations"></a><span data-ttu-id="6cf79-103">Virkja ráðleggingar um „versla svipaða lýsingu“</span><span class="sxs-lookup"><span data-stu-id="6cf79-103">Enable "shop similar description" recommendations</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="6cf79-104">Þetta efnisatriði lýsir því hvernig á að virkja vörutillögurnar fyrir „versla vörur með svipaðri lýsingu“ í Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="6cf79-104">This topic describes how to enable "shop similar description" product recommendations in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="6cf79-105">Eiginleikinn fyrir tillögu um „versla vörur með svipaðri lýsingu“ í Dynamics 365 Commerce notar gervigreind og vélnám til að koma með tillögur að vörum sem eru með svipaðar lýsingar og það sem viðskiptavinurinn er að skoða.</span><span class="sxs-lookup"><span data-stu-id="6cf79-105">The "shop similar description" recommendations feature in Dynamics 365 Commerce uses artificial intelligence and machine learning (AI-ML) to deliver recommendations for products that have descriptions that are similar to what the customer is looking for.</span></span> <span data-ttu-id="6cf79-106">Með því að bjóða upp á tillögur fyrir „versla vörur með svipaðri lýsingu“ fyrir allar smásölurásir í Commerce, geta smásalar auðveldað viðskiptavinum að finna það sem þeir vilja.</span><span class="sxs-lookup"><span data-stu-id="6cf79-106">By making "shop similar description" recommendations available for all retail channels in Commerce, retailers can help customers easily find what they want.</span></span>

<span data-ttu-id="6cf79-107">Virknin fyrir tillögur um „versla vörur með svipaðri lýsingu“ notar vöruheiti og lýsingu á grunnvöru til að finna og mæla með svipuðum vörum í vörulista smásöluaðilans.</span><span class="sxs-lookup"><span data-stu-id="6cf79-107">The functionality for "shop similar description" recommendations uses the product name and description of seed products to find and recommend similar products in a retailer's product catalog.</span></span>

<span data-ttu-id="6cf79-108">Tillögur fyrir „versla vörur með svipaðri lýsingu“ er í boði bæði á sölustað og í rafrænni viðskiptaupplifun.</span><span class="sxs-lookup"><span data-stu-id="6cf79-108">"Shop similar description" recommendations are available in both the point of sale (POS) and e-commerce experiences.</span></span>

## <a name="example-scenarios"></a><span data-ttu-id="6cf79-109">Dæmi um aðstæður</span><span class="sxs-lookup"><span data-stu-id="6cf79-109">Example scenarios</span></span>

<span data-ttu-id="6cf79-110">Eftirfarandi dæmi um aðstæður sýnir tillögugerðir sem virknin „versla vörur með svipaðri lýsingu“ getur boðið upp á:</span><span class="sxs-lookup"><span data-stu-id="6cf79-110">The following example scenarios show the types of recommendations that the "shop similar description" functionality can provide:</span></span>

- <span data-ttu-id="6cf79-111">Viðskiptavinur skoðar gamaldags hornspangagleraugu og fær nokkrar tillögur að öðrum gleraugum sem eru með svipaða hönnun innan sviðs smásöluaðilans.</span><span class="sxs-lookup"><span data-stu-id="6cf79-111">A customer views a pair of retro-style horn-rimmed glasses and receives a set of recommendations for other glasses that have a similar design, in the context of the retailer's industry.</span></span>
- <span data-ttu-id="6cf79-112">Viðskiptavinur notar tillögur að „versla vörur með svipaða lýsingu“ til að uppgötva kaffitegundir sem eru með svipað bragð og hann keypti áður hjá smásöluaðilanum.</span><span class="sxs-lookup"><span data-stu-id="6cf79-112">A customer uses "shop similar description" recommendations to discover coffee flavors that are similar to a flavor that they previously purchased from the retailer.</span></span>

## <a name="set-up-shop-similar-description-recommendations"></a><span data-ttu-id="6cf79-113">Setja upp tilllögur að „versla vörur með svipaðri lýsingu“</span><span class="sxs-lookup"><span data-stu-id="6cf79-113">Set up "shop similar description" recommendations</span></span>

<span data-ttu-id="6cf79-114">Vöruráðleggingar eru aðeins studdar fyrir notendur Commerce sem hafa flutt geymsluna sína til Azure Data Lake Storage Gen2.</span><span class="sxs-lookup"><span data-stu-id="6cf79-114">Product recommendations are supported only for Commerce users who have migrated their storage to Azure Data Lake Storage Gen2.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="6cf79-115">Forkröfur</span><span class="sxs-lookup"><span data-stu-id="6cf79-115">Prerequisites</span></span>

<span data-ttu-id="6cf79-116">Áður en hægt er að sýna viðskiptavinum ráðleggingar um „versla vörur með svipaðri lýsingu“ þarf að ljúka eftirfarandi skilyrðum:</span><span class="sxs-lookup"><span data-stu-id="6cf79-116">Before "shop similar description" recommendations can be shown to customers, you must complete the following prerequisites:</span></span>

- <span data-ttu-id="6cf79-117">[Virkja ráðleggingar um afurðir](enable-product-recommendations.md) í Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="6cf79-117">[Enable product recommendations](enable-product-recommendations.md) in Commerce headquarters.</span></span>
- <span data-ttu-id="6cf79-118">Staðfestið að miðlaþjónninn styðji HTTP-köll.</span><span class="sxs-lookup"><span data-stu-id="6cf79-118">Confirm that the media server supports HTTPS calls.</span></span>

### <a name="turn-on-the-shop-similar-description-recommendations-feature"></a><span data-ttu-id="6cf79-119">Kveikja á eiginleika fyrir ráðleggingar um „versla vörur með svipaðri lýsingu“</span><span class="sxs-lookup"><span data-stu-id="6cf79-119">Turn on the "shop similar description" recommendations feature</span></span>

<span data-ttu-id="6cf79-120">Til að kveikja á eiginleika fyrir ráðleggingar um „versla vörur með svipaðri lýsingu“ í Commerce Headquarters skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="6cf79-120">To turn on the "shop similar description" recommendations feature in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="6cf79-121">Á vinnusvæðinu **Eiginleikastjórnun**, í lista yfir tiltæka eiginleika, skal leita að og velja **Versla vörur með svipaða lýsingu**.</span><span class="sxs-lookup"><span data-stu-id="6cf79-121">In the **Feature management** workspace, in the list of available features, search for and select **Shop similar description**.</span></span>
1. <span data-ttu-id="6cf79-122">Í glugganum hægra megin skal velja **Virkja**.</span><span class="sxs-lookup"><span data-stu-id="6cf79-122">In the right pane, select **Enable**.</span></span>

> [!NOTE]
> <span data-ttu-id="6cf79-123">Þegar kveikt er á eiginleikanum byrjar kerfið að búa til tillögulista yfir vörur.</span><span class="sxs-lookup"><span data-stu-id="6cf79-123">When you turn on the feature, the system starts to generate product recommendation lists.</span></span> <span data-ttu-id="6cf79-124">Það getur tekið allt að einn dag áður en listarnir verða aðgengilegir og sýnilegir á netinu og í afgreiðslukössum.</span><span class="sxs-lookup"><span data-stu-id="6cf79-124">It might take up to a day for those lists to become available and visible online and on POS terminals.</span></span>
>
> <span data-ttu-id="6cf79-125">Ef slökkt er á eiginleikanum mun það ekki hafa áhrif á aðrar gerðir af vörutillögum.</span><span class="sxs-lookup"><span data-stu-id="6cf79-125">If you turn off the feature, other types of product recommendations aren't affected.</span></span> <span data-ttu-id="6cf79-126">Frekari upplýsingar um vörutillögur er að finna í [Yfirlit yfir vöruráðleggingar](product-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="6cf79-126">For more information about product recommendations, see [Product recommendations overview](product-recommendations.md).</span></span>

## <a name="add-a-shop-similar-description-button-to-product-details-pages"></a><span data-ttu-id="6cf79-127">Bæta hnappi fyrir versla vörur með svipaða lýsingu á síður vöruupplýsinga</span><span class="sxs-lookup"><span data-stu-id="6cf79-127">Add a Shop similar description button to product details pages</span></span>

<span data-ttu-id="6cf79-128">Þegar kveikt hefur verið á eiginleikanum fyrir tillögur að „versla vörur með svipaða lýsingu“ í Commerce Headquarters er hægt að bæta hnappnum **Versla vörur með svipaða lýsingu** við kaupglugga hvaða vöruupplýsingasíðu sem er.</span><span class="sxs-lookup"><span data-stu-id="6cf79-128">After you turn on the "shop similar description" recommendations feature in Commerce headquarters, you can add a **Shop similar description** button to the buy box on any product details page (PDP).</span></span> <span data-ttu-id="6cf79-129">Viðskiptavinur sem velur þennan hnapp er vísað á viðeigandi síðu **Versla vörur með svipaða lýsingu** sem sýnir vörur sem eru svipaðar útlits.</span><span class="sxs-lookup"><span data-stu-id="6cf79-129">A customer who selects this button is taken to a dedicated **Shop similar description** page that shows visually similar products.</span></span> <span data-ttu-id="6cf79-130">Viðskiptavinurinn getur síðan notað val til að afmarka vörurnar enn frekar.</span><span class="sxs-lookup"><span data-stu-id="6cf79-130">The customer can then use selectors to further filter the products.</span></span>

<span data-ttu-id="6cf79-131">Til að bæta hnappnum **Versla vörur með svipaða lýsingu** við upplýsingasíðu afurðar með því að nota Commerce Site Builder, skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="6cf79-131">To add a **Shop similar description** button to a PDP by using Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="6cf79-132">Opnið fyrirliggjandi síðu svæðishönnunar sem inniheldur kaupgluggaeiningu.</span><span class="sxs-lookup"><span data-stu-id="6cf79-132">Open an existing site builder page that contains a buy box module.</span></span>
1. <span data-ttu-id="6cf79-133">Á vinstra yfirlitssvæðinu skal velja kaupgluggaeininguna.</span><span class="sxs-lookup"><span data-stu-id="6cf79-133">In the left navigation pane, select the buy box module.</span></span>
1. <span data-ttu-id="6cf79-134">Á hægra yfirlitssvæðinu skal velja gátreitinn **Virkja tengil til að kaupa vörur með svipaða lýsingu**.</span><span class="sxs-lookup"><span data-stu-id="6cf79-134">In the right pane, select the **Enable Shop Similar description Link** check box.</span></span>
1. <span data-ttu-id="6cf79-135">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="6cf79-135">Select **Save**.</span></span>
1. <span data-ttu-id="6cf79-136">Veldu **Ljúka við breytingar** til að athuga á síðunni og veldu síðan **Birta** til að birta hana.</span><span class="sxs-lookup"><span data-stu-id="6cf79-136">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span> <span data-ttu-id="6cf79-137">Þegar síðan hefur verið birt mun upplýsingasíða afurðar innihalda hnappinn **Versla vörur með svipaða lýsingu**.</span><span class="sxs-lookup"><span data-stu-id="6cf79-137">After the page is published, the PDP will include a **Shop similar description** button.</span></span>

<span data-ttu-id="6cf79-138">Eftirfarandi mynd sýnir gátreitinn **Virkja tengil til að versla vörur með svipaða lýsingu** og hnappinn **Versla vörur með svipaða lýsingu** í dæmi um upplýsingasíðu afurðar í svæðishönnuði.</span><span class="sxs-lookup"><span data-stu-id="6cf79-138">The following illustration shows the **Enable shop similar description Link** check box and the **Shop similar description** button on an example PDP in site builder.</span></span>

![Gátreiturinn „Virkja tengil til að versla vörur með svipaða lýsingu“ og hnappurinn „Versla vörur með svipaða lýsingu“ á upplýsingasíðu afurðar í svæðishönnuði](./media/ter_site_builder_buybox_button.png)

## <a name="additional-resources"></a><span data-ttu-id="6cf79-140">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="6cf79-140">Additional resources</span></span>

[<span data-ttu-id="6cf79-141">Yfirlit yfir afurðarráðleggingar</span><span class="sxs-lookup"><span data-stu-id="6cf79-141">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="6cf79-142">Virkja Azure Data Lake Storage í Dynamics 365 Commerce-umhverfi</span><span class="sxs-lookup"><span data-stu-id="6cf79-142">Enable Azure Data Lake Storage in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="6cf79-143">Virkja ráðleggingar um afurðir</span><span class="sxs-lookup"><span data-stu-id="6cf79-143">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="6cf79-144">Virkja tillögur um að kaupa svipaða vöru</span><span class="sxs-lookup"><span data-stu-id="6cf79-144">Enable "shop similar looks" recommendations</span></span>](shop-similar-looks.md)

[<span data-ttu-id="6cf79-145">Aðlagaðu niðurstöður AI-ML</span><span class="sxs-lookup"><span data-stu-id="6cf79-145">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="6cf79-146">Búðu til handvirkt myndaðar ráðleggingar</span><span class="sxs-lookup"><span data-stu-id="6cf79-146">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="6cf79-147">Algengar spurningar um afurðaráðleggingar</span><span class="sxs-lookup"><span data-stu-id="6cf79-147">Product recommendations FAQ</span></span>](faq-recommendations.md)
