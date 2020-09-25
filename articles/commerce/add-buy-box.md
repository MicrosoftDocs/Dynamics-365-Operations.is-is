---
title: Kaupkassaeining
description: Þetta efni fjallar um kaupakassaeiningar og lýsir því hvernig á að bæta þeim við vefsíður hjá Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 08/31/2020
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
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 6556ee8acf1e24a9f6ceddb622960cb3ac891852
ms.sourcegitcommit: 420b9e538f706178f8e1f2786e02f4f400bf2336
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/02/2020
ms.locfileid: "3761298"
---
# <a name="buy-box-module"></a><span data-ttu-id="d72ab-103">Kaupkassaeining</span><span class="sxs-lookup"><span data-stu-id="d72ab-103">Buy box module</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="d72ab-104">Þetta efni fjallar um kaupakassaeiningar og lýsir því hvernig á að bæta þeim við vefsíður hjá Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="d72ab-104">This topic covers buy box modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="d72ab-105">Yfirlit</span><span class="sxs-lookup"><span data-stu-id="d72ab-105">Overview</span></span>

<span data-ttu-id="d72ab-106">Hugtakið *kaupkassi* vísar venjulega til svæðisins á vöruupplýsingasíðunni sem er „yfir brotinu“ og hýsir allar mikilvægustu upplýsingarnar sem þarf til að kaupa vöru.</span><span class="sxs-lookup"><span data-stu-id="d72ab-106">The term *buy box* typically refers to the area of a product details page that is "above the fold," and that hosts all the most important information that is required to make a product purchase.</span></span> <span data-ttu-id="d72ab-107">(Svæði sem er „fyrir ofan brotið“ er sýnilegt þegar síðunni er fyrst hlaðið þannig að notendur þurfa ekki að fletta niður til að sjá hana.)</span><span class="sxs-lookup"><span data-stu-id="d72ab-107">(An area that is "above the fold" is visible when the page is first loaded, so that users don't have to scroll down to see it.)</span></span>

<span data-ttu-id="d72ab-108">Kaupkassaeining er sérstakur gámur sem er notaður til að hýsa allar einingar sem sýndar eru á kaupkassasvæðinu á upplýsingasíðu vöru.</span><span class="sxs-lookup"><span data-stu-id="d72ab-108">A buy box module is special container that is used to host all the modules that are shown in the buy box area of a product details page.</span></span>

<span data-ttu-id="d72ab-109">Vefslóð upplýsingasíðu inniheldur afurðakennið.</span><span class="sxs-lookup"><span data-stu-id="d72ab-109">The URL of a product details page includes the product ID.</span></span> <span data-ttu-id="d72ab-110">Allar upplýsingar sem krafist er til að skila kaupkassaeiningar eru dregnar af þessu afurðakenni.</span><span class="sxs-lookup"><span data-stu-id="d72ab-110">All the information that is required to render a buy box module is derived from this product ID.</span></span> <span data-ttu-id="d72ab-111">Ef afurðakenni er ekki gefið upp verður kaupkassaeiningin ekki gefin rétt upp á síðu.</span><span class="sxs-lookup"><span data-stu-id="d72ab-111">If a product ID isn't provided, the buy box module won't be rendered correctly on a page.</span></span> <span data-ttu-id="d72ab-112">Þess vegna er aðeins hægt að nota innkaupakassaeiningar á síðum sem eru með samhengi vöru.</span><span class="sxs-lookup"><span data-stu-id="d72ab-112">Therefore, a buy box module can be used only on pages that have product context.</span></span> <span data-ttu-id="d72ab-113">Til að nota það á síðu sem er ekki með samhengi vöru (til dæmis heimasíðu eða markaðssíðu) verður þú að gera viðbótarstillingar.</span><span class="sxs-lookup"><span data-stu-id="d72ab-113">To use it on a page that doesn't have product context (for example, a home page or a marketing page), you must do additional customizations.</span></span>

<span data-ttu-id="d72ab-114">Eftirfarandi mynd sýnir dæmi um kaupgluggaeiningu á upplýsingasíðu afurðar.</span><span class="sxs-lookup"><span data-stu-id="d72ab-114">The following image shows an example of a buy box module on a product details page.</span></span>

![Dæmi um kaupgluggaeiningu](./media/ecommerce-pdp-buybox.PNG)

## <a name="buy-box-module-properties-and-slots"></a><span data-ttu-id="d72ab-116">Eiginleikar og hólf kaupkassaeininga</span><span class="sxs-lookup"><span data-stu-id="d72ab-116">Buy box module properties and slots</span></span> 

<span data-ttu-id="d72ab-117">Á vöruupplýsingasíðu er kaupkassa skipt í tvö svæði: miðlasvæði til vinstri og innihaldssvæði til hægri.</span><span class="sxs-lookup"><span data-stu-id="d72ab-117">On a product details page, a buy box is divided into two regions: a media region on the left and a content region on the right.</span></span> <span data-ttu-id="d72ab-118">Sjálfgefið er að hlutfall breiddar dálks fjölmiðlasvæðisins og breiddar dálks innihaldssvæðisins sé 2:1.</span><span class="sxs-lookup"><span data-stu-id="d72ab-118">By default, the ratio of the width of the media region column to the width of the content region column is 2:1.</span></span> <span data-ttu-id="d72ab-119">Í fartækjum er svæðunum tveimur staflað, þannig að eitt svæði birtist fyrir neðan hitt svæðið.</span><span class="sxs-lookup"><span data-stu-id="d72ab-119">On mobile devices, the two regions are stacked so that one region appears below the other region.</span></span> <span data-ttu-id="d72ab-120">Hægt er að nota þemu til að sérsníða súlubreidd og staflaröðun.</span><span class="sxs-lookup"><span data-stu-id="d72ab-120">Themes can be used to customize the column widths and stacking rank.</span></span>

<span data-ttu-id="d72ab-121">Kaupkassaeining gefur titil, lýsingu, verð og einkunnir afurðar.</span><span class="sxs-lookup"><span data-stu-id="d72ab-121">A buy box module renders the title, description, price, and ratings of a product.</span></span> <span data-ttu-id="d72ab-122">Hún gerir viðskiptavinum einnig kleift að velja vöruafbrigði sem hafa mismunandi afurðareigindir, svo sem stærð, stíl og lit.</span><span class="sxs-lookup"><span data-stu-id="d72ab-122">It also lets customers select product variants that have different product attributes, such as size, style, and color.</span></span> <span data-ttu-id="d72ab-123">Þegar afurðarafbrigði er valið eru aðrir eiginleikar í kaupkassanum (til dæmis afurðarlýsingin og myndirnar) uppfærðir til að endurspegla upplýsingar um afbrigðið.</span><span class="sxs-lookup"><span data-stu-id="d72ab-123">When a product variant is selected, other properties in the buy box (for example, the product description and images) are updated to reflect the variant information.</span></span> 

<span data-ttu-id="d72ab-124">Magnval er veitt svo að viðskiptavinir geti tilgreint magn varanna sem á að kaupa.</span><span class="sxs-lookup"><span data-stu-id="d72ab-124">A quantity selector is provided, so that customers can specify the quantity of items to purchase.</span></span> <span data-ttu-id="d72ab-125">Hægt er að skilgreina hámarksmagn sem hægt er að kaupa í stillingum vefsvæðisins.</span><span class="sxs-lookup"><span data-stu-id="d72ab-125">The maximum quantity that can be purchased can be defined in the site settings.</span></span>

<span data-ttu-id="d72ab-126">Í kaupboxinu geta viðskiptavinir einnig framkvæmt aðgerðir eins og að bæta vöru við körfuna, bæta vöru við óskalistann sinn og velja afhendingarstað.</span><span class="sxs-lookup"><span data-stu-id="d72ab-126">From the buy box, customers can also perform actions such as adding a product to the cart, adding a product to their wishlist, and selecting a pickup location.</span></span> <span data-ttu-id="d72ab-127">Þessar aðgerðir er hægt að framkvæma á afurð eða afurðarafbrigði.</span><span class="sxs-lookup"><span data-stu-id="d72ab-127">These actions can be performed on a product or a product variant.</span></span> <span data-ttu-id="d72ab-128">Til að bæta afurð við óskalista verður viðskiptavinurinn að vera skráður inn.</span><span class="sxs-lookup"><span data-stu-id="d72ab-128">To add a product to a wishlist, the customer must be signed in.</span></span>

<span data-ttu-id="d72ab-129">Þemu er hægt að nota til að fjarlægja eða breyta röð afurðaeiginleika og aðgerðastýringa kaupkassa.</span><span class="sxs-lookup"><span data-stu-id="d72ab-129">Themes can be used to remove or change the order of buy box product properties and action controls.</span></span> 

## <a name="module-properties"></a><span data-ttu-id="d72ab-130">Eiginleikar einingar</span><span class="sxs-lookup"><span data-stu-id="d72ab-130">Module properties</span></span>

- <span data-ttu-id="d72ab-131">**Merki fyrirsagna** – Þessi eiginleiki skilgreinir merki fyrirsagna fyrir afurðarheitið.</span><span class="sxs-lookup"><span data-stu-id="d72ab-131">**Heading tag** – This property defines the heading tag for the product title.</span></span> <span data-ttu-id="d72ab-132">Ef kaupkassinn er efst á síðunni ætti að stilla þennan eiginleika á **h1** til að uppfylla aðgengisstaðla.</span><span class="sxs-lookup"><span data-stu-id="d72ab-132">If the buy box is at the top of the page, this property should be set to **h1** to meet accessibility standards.</span></span> 

- <span data-ttu-id="d72ab-133">**Virkja tillögur um að kaupa svipaða vöru** - Þessi eiginleiki heimilar kaupreit að sýna tengla á vörur sem svipar til atriðisins sem er skoðað.</span><span class="sxs-lookup"><span data-stu-id="d72ab-133">**Enable "shop similar looks" recommendations** - This property allows the buy box to show links to products that look similar to the currently viewed item.</span></span> <span data-ttu-id="d72ab-134">Þessi eiginleiki er tiltækur í Commerce Release 10.0.13 og nýrri.</span><span class="sxs-lookup"><span data-stu-id="d72ab-134">This feature is available in Commerce release 10.0.13 and later.</span></span>

## <a name="modules-that-can-be-used-in-a-buy-box-module"></a><span data-ttu-id="d72ab-135">Einingar sem hægt er að nota í kaupkassaeiningu</span><span class="sxs-lookup"><span data-stu-id="d72ab-135">Modules that can be used in a buy box module</span></span>

- <span data-ttu-id="d72ab-136">**Miðlasafn** - Þessi eining er notuð til að sýna myndir af afurð á upplýsingasíðu afurðar.</span><span class="sxs-lookup"><span data-stu-id="d72ab-136">**Media gallery** – This module is used to showcase images of a product on a product details page.</span></span> <span data-ttu-id="d72ab-137">Frekari upplýsingar um þessa einingu er að finna í [Eining efnissafns](media-gallery-module.md).</span><span class="sxs-lookup"><span data-stu-id="d72ab-137">For more information about this module, see [Media gallery module](media-gallery-module.md).</span></span>
- <span data-ttu-id="d72ab-138">**Verslunarval** – Þessi eining sýnir lista yfir nærliggjandi verslanir þar sem hægt er að sækja vöru.</span><span class="sxs-lookup"><span data-stu-id="d72ab-138">**Store selector** – This module shows a list of nearby stores where an item is available for pickup.</span></span> <span data-ttu-id="d72ab-139">Það gerir notendum kleift að slá inn staðsetningu til að finna verslanir í nágrenninu.</span><span class="sxs-lookup"><span data-stu-id="d72ab-139">It lets users enter a location to find stores that are nearby.</span></span> <span data-ttu-id="d72ab-140">Frekari upplýsingar um þessa einingu er að finna í [Verslunarvalseining](store-selector.md).</span><span class="sxs-lookup"><span data-stu-id="d72ab-140">For more information about this module, see [Store selector module](store-selector.md).</span></span>
- <span data-ttu-id="d72ab-141">**Samfélagsmiðlar** - Þessari einingu er hægt að bæta við kaupreitinn til að gera notendum kleift að miðla upplýsingum um vöru á samfélagsmiðlum.</span><span class="sxs-lookup"><span data-stu-id="d72ab-141">**Social share** - This module can be added to the buy box to allow users to share product information on social media.</span></span> <span data-ttu-id="d72ab-142">Nánari upplýsingar eru í [Samfélagsmiðlaeining](social-share-module.md).</span><span class="sxs-lookup"><span data-stu-id="d72ab-142">For more information, see [Social share module](social-share-module.md).</span></span>

## <a name="buy-box-module-settings"></a><span data-ttu-id="d72ab-143">Stillingar kaupkassaeiningar</span><span class="sxs-lookup"><span data-stu-id="d72ab-143">Buy box module settings</span></span>

<span data-ttu-id="d72ab-144">Hægt er að skilgreina eftirfarandi stillingar fyrir kaupgluggaeiningar á **Stillingar svæðis \> viðbætur**:</span><span class="sxs-lookup"><span data-stu-id="d72ab-144">The following buy box module settings can be configured at **Site Settings \> Extensions**:</span></span>

- <span data-ttu-id="d72ab-145">**Hámarksmagn körfulínu** - Þessi eiginleiki er notaður til að sýna hámarksfjölda hverrar vöru sem hægt er að bæta við körfuna.</span><span class="sxs-lookup"><span data-stu-id="d72ab-145">**Cart line quantity limit** – This property is used to specify the maximum number of each item that can be added to the cart.</span></span> <span data-ttu-id="d72ab-146">Til dæmis gæti smásali ákveðið að aðeins megi selja 10 stykki af hverri afurð í sömu færslunni.</span><span class="sxs-lookup"><span data-stu-id="d72ab-146">For example, a retailer might decide that only 10 of each product can be sold in a single transaction.</span></span>
- <span data-ttu-id="d72ab-147">**Birgðir** - Frekari upplýsingar um hvernig á að nota birgðastillingar er að finna í [Nota birgðastillingar](inventory-settings.md).</span><span class="sxs-lookup"><span data-stu-id="d72ab-147">**Inventory** – For information about how to apply inventory settings, see [Apply inventory settings](inventory-settings.md).</span></span>
- <span data-ttu-id="d72ab-148">**Bæta í körfu** - Þessi eiginleiki er notaður til að sýna hegðun eftir að vöru hefur verið bætt í körfuna.</span><span class="sxs-lookup"><span data-stu-id="d72ab-148">**Add to cart** - This property is used to specify the behavior after an item is added to the cart.</span></span> <span data-ttu-id="d72ab-149">Mögulegu gildin eru **Fara í körfu**, **Ekki fara í körfu** og **Sýna tilkynningar**.</span><span class="sxs-lookup"><span data-stu-id="d72ab-149">The possible values are **Navigate to cart**, **Do not navigate to cart**, and **Show notifications**.</span></span> <span data-ttu-id="d72ab-150">Þegar gildið er stillt á **Fara í körfu** er notendum vísað á körfusíðuna eftir að hafa bætt við vöru.</span><span class="sxs-lookup"><span data-stu-id="d72ab-150">When the value is set to **Navigate to cart**, users are sent to the cart page after they add an item.</span></span> <span data-ttu-id="d72ab-151">Þegar gildið er stillt á **Ekki fara í körfu** er notendum ekki vísað á körfusíðuna eftir að hafa bætt við vöru.</span><span class="sxs-lookup"><span data-stu-id="d72ab-151">When the value is set to **Do not navigate to cart**, users aren't sent to the cart page after they add an item.</span></span> <span data-ttu-id="d72ab-152">Þegar gildið er stillt á **Sýna tilkynningar** fá notendur staðfestingu og geta haldið áfram að vafra á upplýsingasíðu afurðar.</span><span class="sxs-lookup"><span data-stu-id="d72ab-152">When the value is set to **Show notifications**, users are shown a confirmation notification and can continue to browse on the product details page.</span></span> 

    <span data-ttu-id="d72ab-153">Eftirfarandi mynd sýnir dæmi um „bætt í körfu“ tilkynningu á Fabrikam-svæðinu.</span><span class="sxs-lookup"><span data-stu-id="d72ab-153">The following image shows an example of an "added to cart" confirmation notification on the Fabrikam site.</span></span>

    ![Dæmi um tilkynningareining](./media/ecommerce-addtocart-notifications.PNG)

## <a name="commerce-scale-unit-interaction"></a><span data-ttu-id="d72ab-155">Samskipti við Commerce Scale Unit</span><span class="sxs-lookup"><span data-stu-id="d72ab-155">Commerce Scale Unit interaction</span></span>

<span data-ttu-id="d72ab-156">Kaupgluggaeiningin sækir afurðarupplýsingar með því að nota forritunarviðmót Commerce Scale Unit.</span><span class="sxs-lookup"><span data-stu-id="d72ab-156">The buy box module retrieves product information by using Commerce Scale Unit application programming interfaces (APIs).</span></span> <span data-ttu-id="d72ab-157">Afurðakenni af upplýsingasíðu vöru er notað til að sækja allar upplýsingar.</span><span class="sxs-lookup"><span data-stu-id="d72ab-157">The product ID from the product details page is used to retrieve all information.</span></span>

## <a name="add-a-buy-box-module-to-a-page"></a><span data-ttu-id="d72ab-158">Bæta kaupkassaeiningu við síðu</span><span class="sxs-lookup"><span data-stu-id="d72ab-158">Add a buy box module to a page</span></span>

<span data-ttu-id="d72ab-159">Fylgdu þessum skrefum til að bæta kaupkassaeiningu við nýja síðu og stilla nauðsynlega eiginleika.</span><span class="sxs-lookup"><span data-stu-id="d72ab-159">To add a buy box module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="d72ab-160">Farðu í **Brot** og veldu **Nýtt** til að búa til nýtt brot.</span><span class="sxs-lookup"><span data-stu-id="d72ab-160">Go to **Fragments**, and select **New** to create a new fragment.</span></span>
1. <span data-ttu-id="d72ab-161">Í svarglugganum **Nýtt brot** skal velja eininguna **Kaupkassi**.</span><span class="sxs-lookup"><span data-stu-id="d72ab-161">In the **New fragment** dialog box, select the **Buybox** module.</span></span>
1. <span data-ttu-id="d72ab-162">Undir **Heiti brots** skal slá inn heitið **Kaupkassabrot** og síðan velja **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="d72ab-162">Under **Fragment name**, enter the name **Buy box fragment**, and then select **OK**.</span></span>
1. <span data-ttu-id="d72ab-163">Í hólfinu **Efnissafn** í kaupgluggaeiningunni skal velja úrfellingarmerkið (**...**) og síðan velja **Bæta við einingu**.</span><span class="sxs-lookup"><span data-stu-id="d72ab-163">In the **Media Gallery** slot of the buy box module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="d72ab-164">Í glugganum **Bæta við einingu** skal velja eininguna **Efnissafn** og síðan velja **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="d72ab-164">In the **Add Module** dialog box, select the **Media gallery** module, and then select **OK**.</span></span>
1. <span data-ttu-id="d72ab-165">Í hólfinu **Verslunarval** í kaupgluggaeiningunni skal velja úrfellingarmerkið (**...**) og síðan velja **Bæta við einingu**.</span><span class="sxs-lookup"><span data-stu-id="d72ab-165">In the **Store selector** slot of the buy box module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="d72ab-166">Í glugganum **Bæta við einingu** skal velja eininguna **Verslunarval** og síðan velja **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="d72ab-166">In the **Add Module** dialog box, select the **Store selector** module, and then select **OK**.</span></span>
1. <span data-ttu-id="d72ab-167">Veldu **Vista**, síðan **Ljúka við breytingar** til að skila brotinu og veldu síðan **Birta** til að birta það.</span><span class="sxs-lookup"><span data-stu-id="d72ab-167">Select **Save**, select **Finish editing** to check in the fragment, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="d72ab-168">Farðu í **Sniðmát** og veldu **Nýtt** til að búa til nýtt sniðmát.</span><span class="sxs-lookup"><span data-stu-id="d72ab-168">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="d72ab-169">Í svarglugganum **Nýtt sniðmát**, undir **Heiti sniðmáts**, skal slá inn **PDP-sniðmát** og velja síðan **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="d72ab-169">In the **New Template** dialog box, under **Template name**, enter **PDP template**, and then select **OK**.</span></span>
1. <span data-ttu-id="d72ab-170">Í hólfinu **Meginmál**, skal velja úrfellingarmerkið (**...**) og síðan velja **Bæta við einingu**.</span><span class="sxs-lookup"><span data-stu-id="d72ab-170">In the **Body** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="d72ab-171">Í glugganum **Bæta við einingu** skal velja eininguna **Sjálfgefin síða** og síðan velja **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="d72ab-171">In the **Add Module** dialog box, select the **Default Page** module, and then select **OK**.</span></span>
1. <span data-ttu-id="d72ab-172">Í hólfinu **Aðalsvæði** á Sjálfgefin síða skal velja úrfellingarmerkið (**...**) og síðan velja **Bæta við broti**.</span><span class="sxs-lookup"><span data-stu-id="d72ab-172">In the **Main** slot of the default page, select the ellipsis (**...**), and then select **Add fragment**.</span></span>
1. <span data-ttu-id="d72ab-173">Í svarglugganum **Velja brot** skal velja síðubrotið **Kaupkassabrot** sem var búið til áður og síðan velja **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="d72ab-173">In the **Select fragment** dialog box, select the **Buy box fragment** fragment that you created earlier, and then select **OK**.</span></span>
1. <span data-ttu-id="d72ab-174">Veldu **Vista**, síðan **Ljúka við breytingar** til að skila sniðmáti og veldu síðan **Birta** til að birta það.</span><span class="sxs-lookup"><span data-stu-id="d72ab-174">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="d72ab-175">Farðu í **Síður** og veldu **Ný** til að búa til nýja síðu.</span><span class="sxs-lookup"><span data-stu-id="d72ab-175">Go to **Pages**, and select **New** to create a new page.</span></span>
1. <span data-ttu-id="d72ab-176">Í svarglugganum **Velja sniðmát** skal velja sniðmátið **PDP-sniðmát**.</span><span class="sxs-lookup"><span data-stu-id="d72ab-176">In the **Choose a template** dialog box, select the **PDP template** template.</span></span> <span data-ttu-id="d72ab-177">Undir **Síðuheiti** skal færa inn **PDP-síðu** og síðan velja **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="d72ab-177">Under **Page name**, enter **PDP page**, and then select **OK**.</span></span>
1. <span data-ttu-id="d72ab-178">Í hólfinu **Aðalsvæði** á nýju síðunni skal velja úrfellingarmerkið (**...**) og síðan velja **Bæta við broti**.</span><span class="sxs-lookup"><span data-stu-id="d72ab-178">In the **Main** slot of the new page, select the ellipsis (**...**), and then select **Add fragment**.</span></span>
1. <span data-ttu-id="d72ab-179">Í svarglugganum **Velja brot** skal velja síðubrotið **Kaupkassabrot** sem var búið til áður og síðan velja **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="d72ab-179">In the **Select fragment** dialog box, select the **Buy box fragment** fragment that you created earlier, and then select **OK**.</span></span>
1. <span data-ttu-id="d72ab-180">Vistaðu og forskoðaðu síðuna.</span><span class="sxs-lookup"><span data-stu-id="d72ab-180">Save and preview the page.</span></span> <span data-ttu-id="d72ab-181">Bættu færibreytustreng fyrirspurnar **?productid=&lt;product id&gt;** við slóðina á forskoðunarsíðunni.</span><span class="sxs-lookup"><span data-stu-id="d72ab-181">Add the **?productid=&lt;product id&gt;** query string parameter to the URL of the preview page.</span></span> <span data-ttu-id="d72ab-182">Þannig er vörusamhengið notað til að hlaða og birta forskoðunarsíðuna.</span><span class="sxs-lookup"><span data-stu-id="d72ab-182">In that way, the product context is used to load and render the preview page.</span></span>
1. <span data-ttu-id="d72ab-183">Veldu **Vista**, síðan **Ljúka við breytingar** til að skila síðunni og veldu síðan **Birta** til að birta hana.</span><span class="sxs-lookup"><span data-stu-id="d72ab-183">Select **Save**, select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span> <span data-ttu-id="d72ab-184">Kaupkassi ætti að birtast á upplýsingasíðu afurða.</span><span class="sxs-lookup"><span data-stu-id="d72ab-184">A buy box should appear on the product details page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d72ab-185">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="d72ab-185">Additional resources</span></span>

[<span data-ttu-id="d72ab-186">Yfirlit byrjendaeiningar</span><span class="sxs-lookup"><span data-stu-id="d72ab-186">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="d72ab-187">Eining til að velja verslun</span><span class="sxs-lookup"><span data-stu-id="d72ab-187">Store selector module</span></span>](store-selector.md)

[<span data-ttu-id="d72ab-188">Eining efnissafns</span><span class="sxs-lookup"><span data-stu-id="d72ab-188">Media gallery module</span></span>](media-gallery-module.md)

[<span data-ttu-id="d72ab-189">Hólfeining</span><span class="sxs-lookup"><span data-stu-id="d72ab-189">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="d72ab-190">Körfueining</span><span class="sxs-lookup"><span data-stu-id="d72ab-190">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="d72ab-191">Greiðsluferliseining</span><span class="sxs-lookup"><span data-stu-id="d72ab-191">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="d72ab-192">Eining pöntunarstaðfestingar</span><span class="sxs-lookup"><span data-stu-id="d72ab-192">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="d72ab-193">Eining síðuhauss</span><span class="sxs-lookup"><span data-stu-id="d72ab-193">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="d72ab-194">Eining síðufótar</span><span class="sxs-lookup"><span data-stu-id="d72ab-194">Footer module</span></span>](author-footer-module.md)

[<span data-ttu-id="d72ab-195">Samfélagsmiðlaeining</span><span class="sxs-lookup"><span data-stu-id="d72ab-195">Social share module</span></span>](social-share-module.md)

[<span data-ttu-id="d72ab-196">Reikna tiltækar birgðir fyrir smásölurásir</span><span class="sxs-lookup"><span data-stu-id="d72ab-196">Calculate inventory availability for retail channels</span></span>](calculated-inventory-retail-channels.md)
