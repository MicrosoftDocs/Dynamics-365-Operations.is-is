---
title: Setja upp netverslunarrás
description: Þessi grein gefur upplýsingar um netverslanarásir og hvernig setja skal þær upp í Dynamics 365 Commerce.
author: kfend
manager: AnnBe
ms.date: 03/02/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailChannelManagementWorkspace, RetailOnlineStoreList
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 16161
ms.assetid: 646d560c-f856-4701-b4ca-44e357ef09b8
ms.search.region: Global
ms.search.industry: Retail
ms.author: meeram
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: b719e40720b091eec879edf332ab63db710a1ebc
ms.sourcegitcommit: 567132f4e4f7a1d76dccf762068209a42c788b52
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/03/2020
ms.locfileid: "3096895"
---
# <a name="set-up-an-online-store-channel"></a><span data-ttu-id="e87fe-103">Setja upp netverslunarrás</span><span class="sxs-lookup"><span data-stu-id="e87fe-103">Set up an online store channel</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="e87fe-104">Þessi grein gefur upplýsingar um netverslanarásir og hvernig setja skal þær upp í Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="e87fe-104">This article provides information about online store channels and how to set them up in Dynamics 365 Commerce.</span></span>

<span data-ttu-id="e87fe-105">Commerce styður margar smásölurásir.</span><span class="sxs-lookup"><span data-stu-id="e87fe-105">Commerce supports multiple retail channels.</span></span> <span data-ttu-id="e87fe-106">Meðal þessara rásir eru netverslanir, símaver, og smásöluverslanir (einnig kallað hefðbundnar verslanir).</span><span class="sxs-lookup"><span data-stu-id="e87fe-106">These channels include online stores, call centers, and retail stores (also known as brick-and-mortar stores).</span></span> <span data-ttu-id="e87fe-107">Netverslun gefur smásölum viðveru á netinu svo að viðskipavinir þeirra geti keypt afurðir úr netverslun þeirra til viðbótar við smásöluverslanir þeirra.</span><span class="sxs-lookup"><span data-stu-id="e87fe-107">Online stores give an online presence to a retailer, so that customers can purchase products from the retailer's online store in addition to its retail stores.</span></span> <span data-ttu-id="e87fe-108">Ef Viðskiptamenn kaupa afurðir úr netverslun geta þeir fengið þær sendar til sín eða sótt þær í staðbundna verslun.</span><span class="sxs-lookup"><span data-stu-id="e87fe-108">If customers purchase products from the online store, those products can be shipped to them, or the customers can pick the products up at a local store.</span></span> 

<span data-ttu-id="e87fe-109">Stofna netverslun í Commerce-biðlara.</span><span class="sxs-lookup"><span data-stu-id="e87fe-109">You create an online store in the Commerce client.</span></span> <span data-ttu-id="e87fe-110">Þessi netverslun er síðan birt til netverslunar þriðja aðila sem er samþætt við Commerce.</span><span class="sxs-lookup"><span data-stu-id="e87fe-110">This online store is then published to a third-party online store that is integrated with Commerce.</span></span> <span data-ttu-id="e87fe-111">Netverslun þriðja aðila gegnir hlutverki búðarglugga (UI) fyrir netverslunina og veitt val um stjórnkerfi viðskiptavinar (CMS) og UI getu.</span><span class="sxs-lookup"><span data-stu-id="e87fe-111">The third-party online store serves as the storefront (UI) for the online store, and gives you a choice of customer management system (CMS) and UI capabilities.</span></span> <span data-ttu-id="e87fe-112">Nokkrar samþættingar af þessari gerð eru tiltækar.</span><span class="sxs-lookup"><span data-stu-id="e87fe-112">Several integrations of this type are available.</span></span> 

<span data-ttu-id="e87fe-113">Eiginleikar sem eru tilgreindar fyrir netverslunina stýrir atferli netverslunarinnar.</span><span class="sxs-lookup"><span data-stu-id="e87fe-113">The properties that you define for the online store control the behavior of the online store.</span></span> <span data-ttu-id="e87fe-114">Til dæmis skilgreina tegundastigveldi yfirlitsflokks og úthluta því á netverslun.</span><span class="sxs-lookup"><span data-stu-id="e87fe-114">For example, you define the navigation category hierarchy and assign it to the online store.</span></span> <span data-ttu-id="e87fe-115">Þegar netverslun er birt fyrir netverslun þriðja aðila, er tegundastigveldi yfirlitsflokks birt í netútgáfu verslunarinnar.</span><span class="sxs-lookup"><span data-stu-id="e87fe-115">When you publish the online store to the third-party online store, the navigation category hierarchy appears in the online version of the store.</span></span> <span data-ttu-id="e87fe-116">Kaupendur nota síðan tegundastigveldi yfirlitsflokks til að fletta upp netverslunina og til að leita að afurðum.</span><span class="sxs-lookup"><span data-stu-id="e87fe-116">Shoppers then use the navigation category hierarchy to browse the online store and search for products.</span></span> 

<span data-ttu-id="e87fe-117">Til að stofna netverslun, verður að setja upp íhluti sem á að leyfa færslur sem vinna á fyrir verslunina.</span><span class="sxs-lookup"><span data-stu-id="e87fe-117">To create an online store, you must set up the components that enable transactions to be processed for the store.</span></span> <span data-ttu-id="e87fe-118">Til dæmis, þarf að bæta úrvali, nota eigindir og setja upp greiðsluhætti og sendingarmáta.</span><span class="sxs-lookup"><span data-stu-id="e87fe-118">For example, you must add assortments, apply attributes, and set up payment methods and shipping methods.</span></span> <span data-ttu-id="e87fe-119">Einnig er hægt að tilgreina verð, kynningartilboð, afslætti, viðskiptasamninga og sendingu greiðsluskilmála sem eiga við netverslun.</span><span class="sxs-lookup"><span data-stu-id="e87fe-119">You can also define prices, promotions, discounts, trade agreements, and shipping terms that are specific to the online store.</span></span> 

<span data-ttu-id="e87fe-120">Eftir að netverslunin hefur verið birt á netverslun þriðja aðila er hægt að stofna vörulista fyrir netverslunina.</span><span class="sxs-lookup"><span data-stu-id="e87fe-120">After you publish the online store to the third-party online store, you can create product catalogs for the online store.</span></span> <span data-ttu-id="e87fe-121">Afurðir í vörulistanum verða afurðaskráningar í netversluninni.</span><span class="sxs-lookup"><span data-stu-id="e87fe-121">The products in the catalog become product listings in the online store.</span></span> <span data-ttu-id="e87fe-122">Þegar sá sem verslar kaupir afurðir úr netverslun, eru tiltækar birgðir uppfærð og samstillt í á biðlaranum.</span><span class="sxs-lookup"><span data-stu-id="e87fe-122">When a shopper purchases products from the online store, the available inventory is updated and synchronized in the client.</span></span> <span data-ttu-id="e87fe-123">Einnig eru sölupantanir myndaðar fyrir innkaup og send til biðlara fyrir pöntunarupplýsingum og vinnslu.</span><span class="sxs-lookup"><span data-stu-id="e87fe-123">Additionally, sales orders are generated for the purchases, and are sent to the client for order fulfillment and processing.</span></span>

## <a name="set-up-an-online-store"></a><span data-ttu-id="e87fe-124">Uppsetning netverslunar</span><span class="sxs-lookup"><span data-stu-id="e87fe-124">Set up an online store</span></span>

<span data-ttu-id="e87fe-125">Til að setja upp netverslun, Það verður að ljúka eftirfarandi verkum:</span><span class="sxs-lookup"><span data-stu-id="e87fe-125">To set up an online store, you must complete the following tasks.</span></span>

1. <span data-ttu-id="e87fe-126">Stofna netverslun.</span><span class="sxs-lookup"><span data-stu-id="e87fe-126">Create the online store.</span></span>
2. <span data-ttu-id="e87fe-127">Bæti netversluninni við viðeigandi stigveldi fyrirtækis</span><span class="sxs-lookup"><span data-stu-id="e87fe-127">Add the online store to the appropriate organization hierarchies.</span></span>
3. <span data-ttu-id="e87fe-128">Bæta við vöruúrval sem hafa með afurð sem eru í boði í netverslun.</span><span class="sxs-lookup"><span data-stu-id="e87fe-128">Add assortments that include the products that are available in the online store.</span></span>
4. <span data-ttu-id="e87fe-129">Úthluta eða stofna verðflokka fyrir netverslun.</span><span class="sxs-lookup"><span data-stu-id="e87fe-129">Assign or create price groups for the online store.</span></span>
5. <span data-ttu-id="e87fe-130">Setja upp afhendingarmátum sem eru í boði fyrir netversluninni.</span><span class="sxs-lookup"><span data-stu-id="e87fe-130">Set up the modes of delivery that are available for the online store.</span></span>
6. <span data-ttu-id="e87fe-131">Úthluta greiðslumáta sem er viðurkenndir af netverslun.</span><span class="sxs-lookup"><span data-stu-id="e87fe-131">Assign the payment methods that are accepted by the online store.</span></span>
7. <span data-ttu-id="e87fe-132">Ef shoppers til að panta afurðir á netinu og síðan taka þær í staðbundna verslun, úthluta verslun slóðarflokki netverslun.</span><span class="sxs-lookup"><span data-stu-id="e87fe-132">If you allow shoppers to order products online and then pick them up at a local store, assign store locator groups to the online store.</span></span>
8. <span data-ttu-id="e87fe-133">Úthluta eigindum fyrir rásir, afurðir og sölupantanir til netverslun.</span><span class="sxs-lookup"><span data-stu-id="e87fe-133">Assign attributes for channels, products, and sales orders to the online store.</span></span> <span data-ttu-id="e87fe-134">Eigindi rásar eiga við alla netverslun, afurðareigindum eiga við afurðir sem eru í boði í netversluninni og eigindum sölupöntunar eiga við sölupantanir sem eru myndaðar úr netverslun.</span><span class="sxs-lookup"><span data-stu-id="e87fe-134">Channel attributes apply to the whole online store, product attributes apply to the products that are offered in the online store, and sales order attributes apply to the sales orders that are generated from the online store.</span></span>
9. <span data-ttu-id="e87fe-135">Varpa eigindum til að skilgreina eiginleika sem ákvarða hvernig þessar eigindir haga sér á netverslun.</span><span class="sxs-lookup"><span data-stu-id="e87fe-135">Map attributes to define the properties that determine how those attributes behave in the online store.</span></span> <span data-ttu-id="e87fe-136">Til dæmis er hægt að skilgreina eigindir eins og þörf er á eða sem leitanlegar.</span><span class="sxs-lookup"><span data-stu-id="e87fe-136">For example, attributes can be defined as required or searchable.</span></span>
10. <span data-ttu-id="e87fe-137">Birta netverslun til að búa til uppbyggingu verslunar að eigin vali fyrir netverslun þriðja aðila.</span><span class="sxs-lookup"><span data-stu-id="e87fe-137">Publish the online store to generate the store structure on your choice of third-party online store.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="e87fe-138">Áður en hægt er að birta netverslun þarf að setja upp dreifingarstað fyrir hana.</span><span class="sxs-lookup"><span data-stu-id="e87fe-138">Before you publish the online store, you must set up a distribution location for it.</span></span>

## <a name="commerce-channel-navigation-hierarchies"></a><span data-ttu-id="e87fe-139">Yfirlitsstigveldi Commerce-rásar</span><span class="sxs-lookup"><span data-stu-id="e87fe-139">Commerce channel navigation hierarchies</span></span>

<span data-ttu-id="e87fe-140">Áður en hægt er að stofna netverslun þarf að skilgreina yfirlitsstigveldi viðskiptarásar sem á að nota fyrir hana.</span><span class="sxs-lookup"><span data-stu-id="e87fe-140">Before you create an online store, you must define the commerce channel navigation hierarchy that you want to use for it.</span></span> <span data-ttu-id="e87fe-141">Yfirlitsstigveldi viðskiptarásar táknar tegundastigveldi sem birtist í netversluninni eftir verslun er birt.</span><span class="sxs-lookup"><span data-stu-id="e87fe-141">The channel navigation hierarchy represents the category hierarchy that is displayed in the online store after the store is published.</span></span> <span data-ttu-id="e87fe-142">Þegar þú birtir vörulista á netverslun, eru afurðirnar í vörulista varpaðar á flokka í yfirlitsstigveldi rásar.</span><span class="sxs-lookup"><span data-stu-id="e87fe-142">When you publish product catalogs to the online store, the products in the catalog are mapped to the categories in the channel navigation hierarchy.</span></span> <span data-ttu-id="e87fe-143">Stigveldið er notuð af þeim sem versla til að fletta í netversluninni.</span><span class="sxs-lookup"><span data-stu-id="e87fe-143">Shoppers then use the hierarchy to navigate in the online store.</span></span>

## <a name="organization-hierarchies"></a><span data-ttu-id="e87fe-144">Stigveldi fyrirtækis</span><span class="sxs-lookup"><span data-stu-id="e87fe-144">Organization hierarchies</span></span>

<span data-ttu-id="e87fe-145">Fyrirtækjastigveldi eru notuð til að skipuleggja viðskiptarásir og til að sýna venslin á milli fyrirtækja innan samstæðunnar í heild sinni.</span><span class="sxs-lookup"><span data-stu-id="e87fe-145">Organization hierarchies are used to structure commerce channels and to represent the relationships between the organizations that make up your business.</span></span> <span data-ttu-id="e87fe-146">Þegar settar eru upp netverslanir er hægt að bæta þeim við stigveldi fyrirtækis.</span><span class="sxs-lookup"><span data-stu-id="e87fe-146">When you set up online stores, you can add them to an organization hierarchy.</span></span> <span data-ttu-id="e87fe-147">Verslanir samnýta gögn sem er notað fyrir úrval áfyllingar og skýrslugerð.</span><span class="sxs-lookup"><span data-stu-id="e87fe-147">The stores then share the data that is used for assortments, replenishment, and reporting.</span></span> 

<span data-ttu-id="e87fe-148">Þegar stofnað er stigveldi fyrirtækis, er málefni úthlutað til þess.</span><span class="sxs-lookup"><span data-stu-id="e87fe-148">When you create an organization hierarchy, you assign a purpose to it.</span></span> <span data-ttu-id="e87fe-149">Málefni gefur til kynna hvernig stigveldi er notað í uppbyggingu business.</span><span class="sxs-lookup"><span data-stu-id="e87fe-149">The purpose indicates how the hierarchy is used in the business structure.</span></span> <span data-ttu-id="e87fe-150">Hægt er að stofna eitt stigveldi fyrirtækis fyrir verslunaraðgerðir þínar og nota það stigveldi úrval, áfyllingar og skýrslugerð.</span><span class="sxs-lookup"><span data-stu-id="e87fe-150">You can create one organization hierarchy for your store operations, and use that hierarchy for assortments, replenishment, and reporting.</span></span> 

<span data-ttu-id="e87fe-151">Einnig er hægt að stofna sérstakt stigveldi fyrirtækis fyrir hvern tilgang.</span><span class="sxs-lookup"><span data-stu-id="e87fe-151">Alternatively, you can create a separate organization hierarchy for each purpose.</span></span> <span data-ttu-id="e87fe-152">Einnig er hægt að stofna mörg stigveldi sem hafa sama tilgangi og úthluta aðskilinni rás til hvers og eins.</span><span class="sxs-lookup"><span data-stu-id="e87fe-152">You can also create multiple hierarchies that have the same purpose, and assign a separate channel to each one.</span></span> <span data-ttu-id="e87fe-153">Ef ætlunin er að birta vörulista á netverslun, ætti að lágmarki að bæta netverslanir við stigveldi fyrirtækis fyrir úrval.</span><span class="sxs-lookup"><span data-stu-id="e87fe-153">If you plan to publish product catalogs to the online store, you should, at a minimum, add the online store to an organization hierarchy for assortments.</span></span> <span data-ttu-id="e87fe-154">Afurðir í vörulista eru valdar úr úrvali afurða sem eru úthlutað til netverslana.</span><span class="sxs-lookup"><span data-stu-id="e87fe-154">The products in a catalog are selected from the assortments that are assigned to the online store.</span></span> <span data-ttu-id="e87fe-155">Þegar vörulistinn er birtur ber birtingu ferli gildisdagsetninga fyrir úrval sem tengdur er við netverslun með afurðir sem eru í vörulista til að ákvarða hvaða vörur skulu vera tiltækar í netversluninni.</span><span class="sxs-lookup"><span data-stu-id="e87fe-155">When the catalog is published, the publishing process compares the effective dates for the assortment that is assigned to the online store with the products that are included in the catalog to determine which products to make available in the online store.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e87fe-156">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="e87fe-156">Additional resources</span></span>

[<span data-ttu-id="e87fe-157">Skilgreina lénsheiti</span><span class="sxs-lookup"><span data-stu-id="e87fe-157">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="e87fe-158">Uppsetning á nýju vefsvæði fyrir rafræn viðskipti</span><span class="sxs-lookup"><span data-stu-id="e87fe-158">Deploy a new e-Commerce site</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="e87fe-159">Stofna svæði fyrir rafræn viðskipti</span><span class="sxs-lookup"><span data-stu-id="e87fe-159">Create an e-Commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="e87fe-160">Tengja netsvæði við rás</span><span class="sxs-lookup"><span data-stu-id="e87fe-160">Associate an online site with a channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="e87fe-161">Vinna með skrárnar robots.txt</span><span class="sxs-lookup"><span data-stu-id="e87fe-161">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="e87fe-162">Hlaða upp mörgum slóðartilvísunum í einu</span><span class="sxs-lookup"><span data-stu-id="e87fe-162">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="e87fe-163">Setja upp B2C-leigjanda í Commerce</span><span class="sxs-lookup"><span data-stu-id="e87fe-163">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

[<span data-ttu-id="e87fe-164">Setja upp sérsniðnar síður fyrir innskráningu notenda</span><span class="sxs-lookup"><span data-stu-id="e87fe-164">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="e87fe-165">Stilla marga B2C leigjendur í viðskiptaumhverfi</span><span class="sxs-lookup"><span data-stu-id="e87fe-165">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

[<span data-ttu-id="e87fe-166">Bæta við stuðningi fyrir efnisbirtingarnet (CDN)</span><span class="sxs-lookup"><span data-stu-id="e87fe-166">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="e87fe-167">Virkja greiningu á verslun eftir staðsetningu</span><span class="sxs-lookup"><span data-stu-id="e87fe-167">Enable location-based store detection</span></span>](enable-store-detection.md)
