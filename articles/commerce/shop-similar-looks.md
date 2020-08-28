---
title: Virkja tillögur um að kaupa svipaða vöru
description: Þetta efnisatriði lýsir því hvernig á að virkja afurðartillögurnar fyrir „versla svipaða vöru“ í Microsoft Dynamics 365 Commerce.
author: bebeale
manager: AnnBe
ms.date: 08/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 2e57965a1073982a7b6c34b79dbf6e5b90d7ee30
ms.sourcegitcommit: 15c68822f4d412bfc609be31b3702f18c81ea0bc
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/06/2020
ms.locfileid: "3666309"
---
# <a name="enable-shop-similar-looks-recommendations"></a><span data-ttu-id="81083-103">Virkja tillögur um að kaupa svipaða vöru</span><span class="sxs-lookup"><span data-stu-id="81083-103">Enable "shop similar looks" recommendations</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="81083-104">Þetta efnisatriði lýsir því hvernig á að virkja afurðartillögurnar fyrir „versla svipaða vöru“ í Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="81083-104">This topic describes how to enable "shop similar looks" product recommendations in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="81083-105">Yfirlit</span><span class="sxs-lookup"><span data-stu-id="81083-105">Overview</span></span>

<span data-ttu-id="81083-106">Eiginleikinn fyrir ráðleggingar um „versla svipaða vöru“ í Dynamics 365 Commerce notar gervigreind og vélnám til að sýna viðskiptavinum afurðir sem líta svipað út.</span><span class="sxs-lookup"><span data-stu-id="81083-106">The "shop similar looks" recommendations feature in Dynamics 365 Commerce uses the power of artificial intelligence and machine learning (AI-ML) to deliver recommendations for visually similar products to customers.</span></span> <span data-ttu-id="81083-107">Með því að bjóða upp á tillögur fyrir „versla svipaða vöru“ fyrir allar smásölurásir í Commerce, geta smásalar aukið ánægja viðskiptavina með því að hjálpa viðskiptavinum að finna á auðveldan hátt það sem þeir vilja.</span><span class="sxs-lookup"><span data-stu-id="81083-107">By making "shop similar looks" recommendations available for all retail channels in Commerce, retailers can increase customer satisfaction by helping customers easily find what they want.</span></span>

<span data-ttu-id="81083-108">Virknin fyrir tillögur um að „versla svipaða vöru“ notar afurðarmyndir af grunnafbrigði afurðar til að finna og mæla með svipað útlítandi afurðum í vörulista smásala.</span><span class="sxs-lookup"><span data-stu-id="81083-108">The functionality for "shop similar looks" recommendations uses product images of seed product variants to find and recommend visually similar products in a retailer's product catalog.</span></span> 

<span data-ttu-id="81083-109">Tillögur um að „versla svipaða vöru“ eru í boði í bæði umhverfi sölustaðar og rafrænna viðskipta.</span><span class="sxs-lookup"><span data-stu-id="81083-109">"Shop similar looks" recommendations are available in both the point of sale (POS) and e-Commerce experiences.</span></span>

### <a name="example-scenarios"></a><span data-ttu-id="81083-110">Dæmi um aðstæður</span><span class="sxs-lookup"><span data-stu-id="81083-110">Example scenarios</span></span>

- <span data-ttu-id="81083-111">Viðskiptavinur skoðar peysu með svörtum röndum og fær tillögu um svipaða peysu í rauðum lit.</span><span class="sxs-lookup"><span data-stu-id="81083-111">A customer views a black striped sweater and receives a recommendation for a similar sweater in red.</span></span> <span data-ttu-id="81083-112">Viðskiptavinurinn velur ráðlögðu vöruna í staðinn fyrir þá sem var skoðuð fyrst og fær síðan tillögur um svipaðar afurðir og þá rauðu.</span><span class="sxs-lookup"><span data-stu-id="81083-112">The customer selects the recommended product instead of the originally viewed product and then receives recommendations for similar products in red.</span></span> 
- <span data-ttu-id="81083-113">Viðskiptavinur notar „versla svipaða vöru“ tillögurnar til að finna eyrnalokka sem passa við hring sem viðskiptavinurinn hefur áhuga á að kaupa.</span><span class="sxs-lookup"><span data-stu-id="81083-113">A customer uses "shop similar looks" recommendations to discover matching earrings for a ring that the customer is interested in buying.</span></span>

## <a name="enable-shop-similar-looks-recommendations-in-commerce-headquarters"></a><span data-ttu-id="81083-114">Virkja tillögur um að kaupa svipaða vöru í Commerce Headquarters</span><span class="sxs-lookup"><span data-stu-id="81083-114">Enable "shop similar looks" recommendations in Commerce headquarters</span></span>

<span data-ttu-id="81083-115">Vöruráðleggingar eru aðeins studdar fyrir notendur Commerce sem hafa flutt geymsluna sína til Azure Data Lake Gen2.</span><span class="sxs-lookup"><span data-stu-id="81083-115">Product recommendations are supported only for Commerce users who have migrated their storage to Azure Data Lake Gen2.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="81083-116">Forkröfur</span><span class="sxs-lookup"><span data-stu-id="81083-116">Prerequisites</span></span>

<span data-ttu-id="81083-117">Áður en smásalar geta byrjað að sýna viðskiptavinum ráðleggingar um „versla svipaða vöru“, eru tvö undirbúningsskref:</span><span class="sxs-lookup"><span data-stu-id="81083-117">Before retailers can begin to show "shop similar looks" recommendations to customers, there are two prerequisite steps:</span></span>

- <span data-ttu-id="81083-118">[Virkja ráðleggingar um afurðir](enable-product-recommendations.md) í Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="81083-118">[Enable product recommendations](enable-product-recommendations.md) in Commerce headquarters.</span></span>
- <span data-ttu-id="81083-119">Staðfestið að miðlaþjónninn styðji HTTP-köll.</span><span class="sxs-lookup"><span data-stu-id="81083-119">Confirm that the media server supports HTTPS calls.</span></span>

<span data-ttu-id="81083-120">Til að tillöguvélin geti fengið aðgang að afurðarmyndum, verða smásalar að búa til vefslóðir afurða.</span><span class="sxs-lookup"><span data-stu-id="81083-120">For the recommendations engine to access the product images, retailers must generate the product URLs.</span></span> <span data-ttu-id="81083-121">Til að búa til vefslóðir afurða í Commerce Headquarters skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="81083-121">To generate product URLs in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="81083-122">Opnið **Myndir afurða**.</span><span class="sxs-lookup"><span data-stu-id="81083-122">Go to **Product images**.</span></span>
1. <span data-ttu-id="81083-123">Á aðgerðasvæðinu skal velja **Skilgreina sniðmát fyrir miðla**.</span><span class="sxs-lookup"><span data-stu-id="81083-123">On the Action Pane, select **Define media template**.</span></span>
1. <span data-ttu-id="81083-124">Á eiginleikasvæðinu **Skilgreina sniðmát fyrir miðla**, undir **Vefslóðir miðla**, skal velja **Búa til vefslóðir**.</span><span class="sxs-lookup"><span data-stu-id="81083-124">In the **Define media template** properties pane, under **Media URLs**, select **Generate URLs**.</span></span>

> [!NOTE]
> <span data-ttu-id="81083-125">Þegar kveikt er á tillögueiginleikanum fyrir „versla svipaða vöru“, hefst ferlið við að búa til tillögulista afurða.</span><span class="sxs-lookup"><span data-stu-id="81083-125">When you enable the "shop similar looks" recommendations feature, the process of generating product recommendation lists begins.</span></span> <span data-ttu-id="81083-126">Allt að einn dagur getur liðið áður en þessir listar verða í boði og sýnilegir á netinu og í afgreiðslukössum.</span><span class="sxs-lookup"><span data-stu-id="81083-126">Up to a day might be required before those lists are available and visible online and on POS terminals.</span></span>

<span data-ttu-id="81083-127">Til að virkja tillögueiginleikann „versla svipaða vöru“ í Commerce Headquarters skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="81083-127">To enable the "shop similar looks" recommendations feature in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="81083-128">Opnið **Eiginleikastjórnun**.</span><span class="sxs-lookup"><span data-stu-id="81083-128">Go to **Feature management**.</span></span>
1. <span data-ttu-id="81083-129">Í lista yfir tiltæka eiginleika skal leita að og velja **Versla svipaðar vörur**.</span><span class="sxs-lookup"><span data-stu-id="81083-129">In the list of available features, search for and select **Shop similar looks**.</span></span>
1. <span data-ttu-id="81083-130">Í glugganum hægra megin skal velja **Virkja** til að kveikja á þjónustunni.</span><span class="sxs-lookup"><span data-stu-id="81083-130">In the right pane, select **Enable** to turn on the service.</span></span>

<span data-ttu-id="81083-131">Eftirfarandi mynd sýnir eiginleikann **Versla svipaðar vörur** á síðunni **Eiginleikastjórnun** í Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="81083-131">The following illustration shows the **Shop similar looks** feature on the **Feature management** page in Commerce headquarters.</span></span>

![Eiginleikinn „versla svipaðar vörur“ á síðu eiginleikastjórnunar í Commerce Headquarters](./media/enableshopsimilarlooks.png)

<span data-ttu-id="81083-133">Eftir að undanfarandi verkum hefur verið lokið eru afgreiðslukassar sjálfkrafa stækkaðir með samhengissvæði **Versla svipaðar vörur**.</span><span class="sxs-lookup"><span data-stu-id="81083-133">After the preceding tasks been completed, POS terminals are automatically enhanced with a contextual **Shop similar products** panel.</span></span> <span data-ttu-id="81083-134">Með því að velja **Skoða meira** getur notendum afgreiðslukassa verið vísað á síðu „versla svipaðar vörur“ sem hægt er að sía enn frekar.</span><span class="sxs-lookup"><span data-stu-id="81083-134">By selecting **See more**, POS terminal users can be taken to a dedicated "shop similar looks" page that can be filtered further.</span></span>

> [!NOTE]
> <span data-ttu-id="81083-135">Ef slökkt er á tillögueiginleikanum „versla svipaðar vörur“, verða engar aðrar gerðir af vöruráðleggingum fyrir áhrifum.</span><span class="sxs-lookup"><span data-stu-id="81083-135">If you turn off the "shop similar looks" recommendations feature, no other types of product recommendations are affected.</span></span> <span data-ttu-id="81083-136">Frekari upplýsingar um vörutillögur er að finna í [Yfirlit yfir vöruráðleggingar](product-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="81083-136">For more information about product recommendations, see [Product recommendations overview](product-recommendations.md).</span></span>

## <a name="add-a-shop-similar-looks-button-to-product-details-pages-by-using-commerce-site-builder"></a><span data-ttu-id="81083-137">Bæta hnappnum „Versla svipaðar vörur“ við upplýsingasíður afurða með því að nota svæðishönnuð Commerce</span><span class="sxs-lookup"><span data-stu-id="81083-137">Add a Shop similar looks button to product details pages by using Commerce site builder</span></span>

<span data-ttu-id="81083-138">Þegar búið er að virkja ráðleggingareiginleikann „versla svipaðar vörur“ í Commerce Headquarters, býður valkostur í svæðishönnuði Commerce upp á að smásalar bæti hnappnum **Versla svipaðar vörur** við kaupglugga hvaða upplýsingasíðu afurðar sem er.</span><span class="sxs-lookup"><span data-stu-id="81083-138">After you enable the "shop similar looks" recommendations feature in Commerce headquarters, an option in Commerce site builder lets retailers to add a **Shop similar looks** button to the buy box on any product details page (PDP).</span></span> <span data-ttu-id="81083-139">Viðskiptavinur sem velur þennan hnapp er vísað á viðeigandi síðu fyrir „versla svipaðar vörur“ sem skilar vörum með svipuðu útliti.</span><span class="sxs-lookup"><span data-stu-id="81083-139">A customer who selects this button is taken to a dedicated "shop similar looks" page that returns visually similar products.</span></span> <span data-ttu-id="81083-140">Þar getur viðskiptavinurinn notað val til að sía frekar afurðirnar.</span><span class="sxs-lookup"><span data-stu-id="81083-140">There, the customer can use selectors to further filter the products.</span></span>

<span data-ttu-id="81083-141">Til að bæta hnappnum **Versla svipaðar vörur** við upplýsingasíðu afurðar með því að nota svæðishönnuð Commerce, skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="81083-141">To add a **Shop similar looks** button to a PDP by using Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="81083-142">Opnið fyrirliggjandi síðu svæðishönnunar sem inniheldur kaupgluggaeiningu.</span><span class="sxs-lookup"><span data-stu-id="81083-142">Open an existing site builder page that contains a buy box module.</span></span>
1. <span data-ttu-id="81083-143">Á vinstra yfirlitssvæðinu skal velja kaupgluggaeininguna.</span><span class="sxs-lookup"><span data-stu-id="81083-143">In the left navigation pane, select the buy box module.</span></span>
1. <span data-ttu-id="81083-144">Á hægri yfirlitssvæðinu skal velja gátreitinn **Virkja tengil til að kaupa svipaða vöru**.</span><span class="sxs-lookup"><span data-stu-id="81083-144">In the right navigation pane, select the **Enable Shop Similar Looks Link** check box.</span></span>
1. <span data-ttu-id="81083-145">Veldu **Vista**, síðan **Ljúka við breytingar** til að skila síðunni og veldu síðan **Birta** til að birta hana.</span><span class="sxs-lookup"><span data-stu-id="81083-145">Select **Save**, select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span> <span data-ttu-id="81083-146">Þegar síðan hefur verið birt mun upplýsingasíða afurðar innihalda hnappinn **Versla svipaðar vörur**.</span><span class="sxs-lookup"><span data-stu-id="81083-146">After the page is published, the PDP will include a **Shop similar looks** button.</span></span>

<span data-ttu-id="81083-147">Eftirfarandi mynd sýnir gátreitinn **Virkja tengil til að kaupa svipaða vöru** og hnappinn **Versla svipaðar vörur** á dæmi um upplýsingasíðu afurðar í svæðishönnuði.</span><span class="sxs-lookup"><span data-stu-id="81083-147">The following illustration shows the **Enable Shop Similar Looks Link** check box and **Shop similar looks** button on an example PDP in site builder.</span></span>

![Gátreiturinn „Virkja tengil til að kaupa svipaða vöru“ og hnappurinn „Versla svipaðar vörur“ á upplýsingasíðu afurðar í svæðishönnuði](./media/SSLecomtooling.png)

## <a name="additional-resources"></a><span data-ttu-id="81083-149">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="81083-149">Additional resources</span></span>

[<span data-ttu-id="81083-150">Yfirlit yfir afurðarráðleggingar</span><span class="sxs-lookup"><span data-stu-id="81083-150">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="81083-151">Virkja Azure Data Lake Storage í Dynamics 365 Commerce-umhverfi</span><span class="sxs-lookup"><span data-stu-id="81083-151">Enable Azure Data Lake Storage in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="81083-152">Virkja ráðleggingar um afurðir</span><span class="sxs-lookup"><span data-stu-id="81083-152">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="81083-153">Afþakka sérsniðnar tillögur</span><span class="sxs-lookup"><span data-stu-id="81083-153">Opt out of personalized recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="81083-154">Bæta afurðaráðleggingum við sölustað</span><span class="sxs-lookup"><span data-stu-id="81083-154">Add product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="81083-155">Bæta við tillögum á færsluskjáinn</span><span class="sxs-lookup"><span data-stu-id="81083-155">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="81083-156">Aðlagaðu niðurstöður AI-ML</span><span class="sxs-lookup"><span data-stu-id="81083-156">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="81083-157">Búðu til handvirkt myndaðar ráðleggingar</span><span class="sxs-lookup"><span data-stu-id="81083-157">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="81083-158">Búðu til tillögur með kynningargögnum</span><span class="sxs-lookup"><span data-stu-id="81083-158">Create recommendations with demo data</span></span>](product-recommendations-demo-data.md)

[<span data-ttu-id="81083-159">Algengar spurningar um afurðaráðleggingar</span><span class="sxs-lookup"><span data-stu-id="81083-159">Product recommendations FAQ</span></span>](faq-recommendations.md)
