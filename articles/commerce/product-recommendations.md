---
title: Yfirlit yfir afurðarráðleggingar
description: Þetta efnisatriði veitir almennar upplýsingar um afurðatillögur. Afurðatillögur auðvelda viðskiptavinum að finna vörur sem þeir vilja á fljótlegan hátt og jafnvel vörur sem þeir ætluðu ekki upphaflega að kaupa.
author: Moonma
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: moonma
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 5aa7db8e53906f9e1416b912fe2c3b70d5430258
ms.sourcegitcommit: 8905d7a7a010e451c5435086480f66650ec54926
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/06/2020
ms.locfileid: "3664883"
---
# <a name="product-recommendations-overview"></a><span data-ttu-id="ca360-104">Yfirlit yfir afurðarráðleggingar</span><span class="sxs-lookup"><span data-stu-id="ca360-104">Product recommendations overview</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="ca360-105">Microsoft Dynamics 365 Commerce má nota til að sýna afurðatillögur á vefsíðu netverslunar og sölustað (POS) tækinu.</span><span class="sxs-lookup"><span data-stu-id="ca360-105">Microsoft Dynamics 365 Commerce can be used to show product recommendations on the e-Commerce website and point of sale (POS) device.</span></span> <span data-ttu-id="ca360-106">Afurðatillögur eru vörur sem viðskiptavinur gæti haft áhuga á.</span><span class="sxs-lookup"><span data-stu-id="ca360-106">Product recommendations are items that a customer might be interested in.</span></span> <span data-ttu-id="ca360-107">Ráðleggingarnar eru byggðar á kaupþróun annarra viðskiptavina í verslunum á netinu og verslunum sjálfum.</span><span class="sxs-lookup"><span data-stu-id="ca360-107">The recommendations are based on the purchase trends of other customers in online and brick-and-mortar stores.</span></span>

<span data-ttu-id="ca360-108">Afurðatillögur gera viðskiptavinum kleift að finna auðveldlega og fljótt vörur sem þeir vilja á meðan þeir hafa reynslu sem þjónar þeim vel.</span><span class="sxs-lookup"><span data-stu-id="ca360-108">Product recommendations allow customers to easily and quickly find products that they want while they have an experience that serves them well.</span></span> <span data-ttu-id="ca360-109">Krosssölu og uppsölu er jafnvel hægt að nota til að hjálpa viðskiptavinum að finna fleiri vörur en þeir ætluðu upphaflega ekki að kaupa.</span><span class="sxs-lookup"><span data-stu-id="ca360-109">Cross-selling and upselling can even be used to assist customers find additional products that they didn't originally intend to buy.</span></span> <span data-ttu-id="ca360-110">Þegar ráðleggingar eru notaðar til að auka uppgötvun vöru skapa þau fleiri viðskiptatækifæri, hjálpað til við að auka sölutekjur og jafnvel aukið ánægju viðskiptavina og varðveisla.</span><span class="sxs-lookup"><span data-stu-id="ca360-110">When recommendations are used to enhance product discovery, they create more conversion opportunities, help increase sales revenue, and even amplify customer satisfaction and retention.</span></span>

<span data-ttu-id="ca360-111">Í Commerce eru afurðatillögur knúnar af vélanámstækni Microsoft tilmæla í stórum stíl.</span><span class="sxs-lookup"><span data-stu-id="ca360-111">In e-Commerce, product recommendations are powered by Microsoft Recommendations machine learning technologies on a large scale.</span></span>

## <a name="recommendation-service"></a><span data-ttu-id="ca360-112">Tillöguþjónusta</span><span class="sxs-lookup"><span data-stu-id="ca360-112">Recommendation service</span></span>

<span data-ttu-id="ca360-113">Vöru ráðleggingarþjónustan notar tækni til gervigreindar og vélanáms (AI-ML) á eftirfarandi hátt:</span><span class="sxs-lookup"><span data-stu-id="ca360-113">The product recommendations service utilizes artificial intelligence and machine learning (AI-ML) technologies in the following way:</span></span>

- <span data-ttu-id="ca360-114">Gögn á sniðinu sem ráðleggingarþjónustan þarf eru dregin út úr virknigagnagrunni Commerce og send til Azure Data Lake Storage eða einingaverslunar.</span><span class="sxs-lookup"><span data-stu-id="ca360-114">Data in the format that the Recommendation service requires is extracted from the Commerce operational database and sent to Azure Data Lake Storage or Entity store.</span></span>
- <span data-ttu-id="ca360-115">Tilmælaþjónustan notar vistuð gögnin til að þjálfa tillögulíkön fyrir listana **Fólki líkar einnig**, **Oft keypt saman**, **Nýtt**, **Mest selt** og **Vinsælt**.</span><span class="sxs-lookup"><span data-stu-id="ca360-115">The recommendations service uses the stored data to train recommendation models for the **People also like**, **Frequently bought together**, **New**, **Best selling**, and **Trending** lists.</span></span>

## <a name="scenarios"></a><span data-ttu-id="ca360-116">Sviðsmyndir</span><span class="sxs-lookup"><span data-stu-id="ca360-116">Scenarios</span></span>

<span data-ttu-id="ca360-117">Afurðatillögur eru í boði fyrir eftirfarandi aðstæður:</span><span class="sxs-lookup"><span data-stu-id="ca360-117">Product recommendations are available for the following scenarios:</span></span>

- <span data-ttu-id="ca360-118">**Á hvaða verslunarsíðu sem er til að vafra eða áfangasíðu í netverslun:** Ef viðskiptavinir eða starfsfólk verslunarinnar heimsækja verslunarsíðu getur meðmælavélin lagt til vörur í listunum **Nýtt**, **Mest selt** og **Vinsælt**.</span><span class="sxs-lookup"><span data-stu-id="ca360-118">**On any store page for browsing or landing page in e-Commerce:** If customers or store associates visit a store page, the recommendation engine can suggest products in the **New**, **Best Selling**, and **Trending** lists.</span></span>
- <span data-ttu-id="ca360-119">**Á síðu vöruupplýsinga:** Ef viðskiptavinir eða starfsfólk verslunar fer á síðuna **Upplýsingar um vöru** mælir tillöguvélin með viðbótarvörum sem einnig er líklegt að verði keyptar.</span><span class="sxs-lookup"><span data-stu-id="ca360-119">**On the Product details page:** If customers or store associates visit a **Product details** page, the recommendation engine suggests additional items that are also likely to be purchased.</span></span> <span data-ttu-id="ca360-120">Þessar vörur birtast á listanum **Fólki líkar einnig**.</span><span class="sxs-lookup"><span data-stu-id="ca360-120">These items appear in the **People also like** list.</span></span>
- <span data-ttu-id="ca360-121">**Á færslusíðunni eða greiðslusíðunni:** Tillöguvélin leggur til vörur, byggðar á öllum listanum yfir vörur í körfunni.</span><span class="sxs-lookup"><span data-stu-id="ca360-121">**On the Transaction page or the checkout page:** The recommendation engine suggests items, based on the whole list of items in the basket.</span></span> <span data-ttu-id="ca360-122">Þessir vörur birtast á listanum **Oft keypt saman**.</span><span class="sxs-lookup"><span data-stu-id="ca360-122">These items appear in the **Frequently bought together** list.</span></span>
- <span data-ttu-id="ca360-123">**Sérsniðnar ráðleggingar:** Vörur geta veitt innskráðum viðskiptavinum persónulega **velur fyrir þig** lista, auk nýrrar virkni sem gerir kleift að sérsníða fyrirliggjandi listasviðsmyndir út frá þeim viðskiptavini.</span><span class="sxs-lookup"><span data-stu-id="ca360-123">**Personalized recommendations:** Merchandizers can provide signed-in customers a personalized **picks for you** list, in addition to new functionality that allows for existing list scenarios to be personalized based on that customer.</span></span> <span data-ttu-id="ca360-124">Til að læra meira, sjál [Kveikja á sérsniðnum tillögum.](personalized-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="ca360-124">To learn more, see [Enable personalized recommendations.](personalized-recommendations.md).</span></span>

### <a name="types-of-product-recommendations"></a><span data-ttu-id="ca360-125">Gerðir afurðarráðlegginga</span><span class="sxs-lookup"><span data-stu-id="ca360-125">Types of product recommendations</span></span>

<span data-ttu-id="ca360-126">Eftirfarandi tafla lýsir ýmsum gerðum sjálfvirkra vöruábendinga sem eru í boði fyrir smásala til að útfæra í þeirra Dynamics 365 Commerce lausn í gegnum [vörusöfnunareining](product-collection-module-overview.md).</span><span class="sxs-lookup"><span data-stu-id="ca360-126">The following table describes various types of automated product recommendations available for retailers to implement in their Dynamics 365 Commerce solution via the [product collection module](product-collection-module-overview.md).</span></span> <span data-ttu-id="ca360-127">Smásalar geta einnig sýnt sérsniðnar niðurstöður fyrir innritaðan notanda ef vefhöfundur velur þann valkost.</span><span class="sxs-lookup"><span data-stu-id="ca360-127">Retailers can also show personalized results for a signed-in user if the site author chooses that option.</span></span>

| <span data-ttu-id="ca360-128">Afurðasafnseining</span><span class="sxs-lookup"><span data-stu-id="ca360-128">Product collection module</span></span>  | <span data-ttu-id="ca360-129">Gerð</span><span class="sxs-lookup"><span data-stu-id="ca360-129">Type</span></span> | <span data-ttu-id="ca360-130">lýsing</span><span class="sxs-lookup"><span data-stu-id="ca360-130">Description</span></span> |
|----------------------------|------|-------------|
| <span data-ttu-id="ca360-131">Nýjar</span><span class="sxs-lookup"><span data-stu-id="ca360-131">New</span></span>                        | <span data-ttu-id="ca360-132">Reiknirit</span><span class="sxs-lookup"><span data-stu-id="ca360-132">Algorithmic</span></span> | <span data-ttu-id="ca360-133">Þessi eining sýnir lista yfir nýjustu afurðirnar sem hafa nýlega verið flokkaðar í rásir og vörulista.</span><span class="sxs-lookup"><span data-stu-id="ca360-133">This module shows a list of the newest products that have been recently assorted to channels and catalogs.</span></span> |
| <span data-ttu-id="ca360-134">Mest selt</span><span class="sxs-lookup"><span data-stu-id="ca360-134">Best selling</span></span>               | <span data-ttu-id="ca360-135">Reiknirit</span><span class="sxs-lookup"><span data-stu-id="ca360-135">Algorithmic</span></span> | <span data-ttu-id="ca360-136">Þessi eining sýnir lista yfir vörur sem eru metnar með mesta sölu.</span><span class="sxs-lookup"><span data-stu-id="ca360-136">This module shows a list of products that are ranked by the highest number of sales.</span></span> |
| <span data-ttu-id="ca360-137">Vinsælt</span><span class="sxs-lookup"><span data-stu-id="ca360-137">Trending</span></span>                   | <span data-ttu-id="ca360-138">Reiknirit</span><span class="sxs-lookup"><span data-stu-id="ca360-138">Algorithmic</span></span> | <span data-ttu-id="ca360-139">Þessi eining sýnir lista yfir vörur sem skila mestum árangri á tilteknu tímabili, raðað eftir mesta sölufjölda.</span><span class="sxs-lookup"><span data-stu-id="ca360-139">This module shows a list of the highest-performing products for a given period, ranked by highest number of sales.</span></span>  |
| <span data-ttu-id="ca360-140">Oft keypt saman</span><span class="sxs-lookup"><span data-stu-id="ca360-140">Frequently bought together</span></span> | <span data-ttu-id="ca360-141">AI-ML</span><span class="sxs-lookup"><span data-stu-id="ca360-141">AI-ML</span></span> | <span data-ttu-id="ca360-142">Þessi eining mælir með lista yfir vörur sem oftast eru keyptar ásamt innihaldi núverandi körfu neytenda.</span><span class="sxs-lookup"><span data-stu-id="ca360-142">This module recommends a list of products that are commonly purchased together with the contents of the consumers current cart.</span></span> |
| <span data-ttu-id="ca360-143">Fólki líkar einnig við</span><span class="sxs-lookup"><span data-stu-id="ca360-143">People also like</span></span>           | <span data-ttu-id="ca360-144">AI-ML</span><span class="sxs-lookup"><span data-stu-id="ca360-144">AI-ML</span></span> | <span data-ttu-id="ca360-145">Þessi eining mælir með vörum fyrir tiltekna grunnafurð byggða á kaupmynstri neytenda.</span><span class="sxs-lookup"><span data-stu-id="ca360-145">This module recommends products for a given seed product based on consumer purchase patterns.</span></span> |
| <span data-ttu-id="ca360-146">Tillögur fyrir þig</span><span class="sxs-lookup"><span data-stu-id="ca360-146">Picks for you</span></span>              | <span data-ttu-id="ca360-147">AI-ML</span><span class="sxs-lookup"><span data-stu-id="ca360-147">AI-ML</span></span> | <span data-ttu-id="ca360-148">Þessi eining mælir með persónulega lista yfir vörur byggðar á innkaupamynstri innritaðs notanda.</span><span class="sxs-lookup"><span data-stu-id="ca360-148">This module recommends a personalized list of products based on purchase patterns of the signed-in user.</span></span> <span data-ttu-id="ca360-149">Fyrir gestanotanda verður þessi listi felldur saman.</span><span class="sxs-lookup"><span data-stu-id="ca360-149">For a guest user, this list will be collapsed.</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="ca360-150">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="ca360-150">Additional resources</span></span>

[<span data-ttu-id="ca360-151">Virkja Azure Data Lake Storage í Dynamics 365 Commerce-umhverfi</span><span class="sxs-lookup"><span data-stu-id="ca360-151">Enable Azure Data Lake Storage in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="ca360-152">Virkja ráðleggingar um afurðir</span><span class="sxs-lookup"><span data-stu-id="ca360-152">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="ca360-153">Kveikja á sérsniðnum tillögum</span><span class="sxs-lookup"><span data-stu-id="ca360-153">Enable personalized recommendations</span></span>](personalized-recommendations.md)

[<span data-ttu-id="ca360-154">Afþakka sérsniðnar tillögur</span><span class="sxs-lookup"><span data-stu-id="ca360-154">Opt out of personalized recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="ca360-155">Virkja tillögur um að kaupa svipaða vöru</span><span class="sxs-lookup"><span data-stu-id="ca360-155">Enable "shop similar looks" recommendations</span></span>](shop-similar-looks.md)

[<span data-ttu-id="ca360-156">Bæta við afurðatillögum á sölustað</span><span class="sxs-lookup"><span data-stu-id="ca360-156">Add product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="ca360-157">Bæta tillögum við færsluskjáinn</span><span class="sxs-lookup"><span data-stu-id="ca360-157">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="ca360-158">Aðlagaðu niðurstöður AI-ML</span><span class="sxs-lookup"><span data-stu-id="ca360-158">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="ca360-159">Búðu til handvirkt myndaðar ráðleggingar</span><span class="sxs-lookup"><span data-stu-id="ca360-159">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="ca360-160">Búðu til tillögur með kynningargögnum</span><span class="sxs-lookup"><span data-stu-id="ca360-160">Create recommendations with demo data</span></span>](product-recommendations-demo-data.md)

[<span data-ttu-id="ca360-161">Algengar spurningar um afurðaráðleggingar</span><span class="sxs-lookup"><span data-stu-id="ca360-161">Product recommendations FAQ</span></span>](faq-recommendations.md)
