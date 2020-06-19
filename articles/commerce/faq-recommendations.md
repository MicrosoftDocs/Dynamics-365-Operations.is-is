---
title: Algengar spurningar um afurðaráðleggingar
description: Þetta efni veitir upplýsingar um ferla og verkfæri sem þú getur notað til að leysa vandamál sem tengjast afurðatillögum eða niðurstöðum þeirra.
author: bebeale
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, Core, Operations
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: e27e4c4d8bdf614d6f55f44daeac3bc152219004
ms.sourcegitcommit: fdc5dd9eb784c7d8e75692c8cdba083fe0dd87ce
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/26/2020
ms.locfileid: "3404303"
---
# <a name="product-recommendations-faq"></a><span data-ttu-id="221aa-103">Algengar spurningar um afurðaráðleggingar</span><span class="sxs-lookup"><span data-stu-id="221aa-103">Product recommendations FAQ</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="221aa-104">Þetta efni veitir upplýsingar um ferla og verkfæri sem þú getur notað til að leysa vandamál sem tengjast [afurðatillögum](product-recommendations.md) eða niðurstöðum þeirra.</span><span class="sxs-lookup"><span data-stu-id="221aa-104">This topic provides information about processes and tools that you can use to troubleshoot issues that are related to [product recommendations](product-recommendations.md) or their results.</span></span>

## <a name="best-practices"></a><span data-ttu-id="221aa-105">Bestu starfsvenjur</span><span class="sxs-lookup"><span data-stu-id="221aa-105">Best practices</span></span>
<span data-ttu-id="221aa-106">Það er mjög mikilvægt að nýta hugtakið afurðarsniðmát og afbrigði.</span><span class="sxs-lookup"><span data-stu-id="221aa-106">It's very important to utilize the concept of product masters and variants.</span></span> <span data-ttu-id="221aa-107">Skynsamleg flokkun afbrigða í yfirafurðarsniðmát hjálpar listum reiknirita og þjónustu við að búa til betri líkön.</span><span class="sxs-lookup"><span data-stu-id="221aa-107">The sensible grouping of variants to a parent product master helps the list algorithms and service create better models.</span></span> <span data-ttu-id="221aa-108">Að auki getur þjónustan þjónað aðeins einu afurðatilviki í stað þess að setja öll náskyld afbrigði á lista.</span><span class="sxs-lookup"><span data-stu-id="221aa-108">Additionally, the service can serve just one instance of a product instead of putting all closely related variants in a list.</span></span> <span data-ttu-id="221aa-109">Þegar öll náskyld afbrigði eru sett á lista geta rangar eða afritaðar niðurstöður komið fram.</span><span class="sxs-lookup"><span data-stu-id="221aa-109">When all closely related variants are put in a list, erroneous or duplicate results can occur.</span></span>

## <a name="why-are-products-missing-from-my-recommendation-lists"></a><span data-ttu-id="221aa-110">Af hverju vantar vörur í tillögulistunum mínum?</span><span class="sxs-lookup"><span data-stu-id="221aa-110">Why are products missing from my recommendation lists?</span></span>

<span data-ttu-id="221aa-111">Venjulega, ef vöru vantar í afurðatillögulista, gæti verið um uppstillingarvandamál að ræða.</span><span class="sxs-lookup"><span data-stu-id="221aa-111">Typically, if an item is missing from a product recommendation list, there might be a product configuration issue.</span></span> <span data-ttu-id="221aa-112">Til dæmis gæti verið um ranga upphafsdagsetningu eða lokadagsetningu að ræða, vídd gæti verið rangt stillt eða varan gæti ekki verið í réttu rásarsamsetningu, o.s.frv.</span><span class="sxs-lookup"><span data-stu-id="221aa-112">For example, there might be an incorrect product start date or end date, a dimension might be misconfigured, or the product might not be in the correct channel assortment, etc.</span></span>

<span data-ttu-id="221aa-113">Ef vöru vantar í tillögulista sem er byggður á námi gervigreindar-véla (AI-ML) gæti varan hugsanlega ekki passað við viðmiðanir tillögulistans, eða það gæti verið að það hafi ekki verið nægjanlegar innkaupafærslur til að tillögulistinn geti sýnt það.</span><span class="sxs-lookup"><span data-stu-id="221aa-113">If an item is missing from a recommendation list that is based on artificial intelligence-machine learning (AI-ML), the item might not fit the criteria of the recommendation list, or it might not have enough purchase transactions for the recommendation list to show it.</span></span>

<span data-ttu-id="221aa-114">Við mælum með að þú athugir þessi skref:</span><span class="sxs-lookup"><span data-stu-id="221aa-114">We recommend that you check these steps:</span></span>
1. <span data-ttu-id="221aa-115">**Gakktu úr skugga um að afurðatillögur hafi verið gerðar virkar í HQ**.</span><span class="sxs-lookup"><span data-stu-id="221aa-115">**Make sure that product recommendations have been enabled in HQ.**</span></span> <span data-ttu-id="221aa-116">Nánari upplýsingar um hvernig hægt er að virkja þessa þjónustu er að finna í [Virkja afurðatillögur](enable-product-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="221aa-116">For more information about how to enable this service, see [Enable product recommendations](enable-product-recommendations.md).</span></span>
1. <span data-ttu-id="221aa-117">**Gakktu úr skugga um að helstu afurðaeiginleikar séu stilltir.**</span><span class="sxs-lookup"><span data-stu-id="221aa-117">**Make sure that key product properties are set.**</span></span> <span data-ttu-id="221aa-118">Til dæmis verður að stilla vöruúrval á **Láta fylgja með**.</span><span class="sxs-lookup"><span data-stu-id="221aa-118">For example, product assortments must be set to **Include**.</span></span>
1. <span data-ttu-id="221aa-119">**Fyrir nýjar valdar vörur getur tekið allt að 3 klukkustundir áður en varan byrjar að birtast á nýja listanum.**</span><span class="sxs-lookup"><span data-stu-id="221aa-119">**For newly assorted products, it might take up to 3 hours before the product will start appearing in the new list.**</span></span>
1. <span data-ttu-id="221aa-120">**Ef vara er enn ekki að birtast í Vinsælt, Mest selt, Fólki líkar líka eða Oft keypt saman, þá gæti verið að sú vara hafi ekki nægar færslur.**</span><span class="sxs-lookup"><span data-stu-id="221aa-120">**If a product is still not appearing in Trending, Best selling, People also like, or Frequently bought together, then that product might not have enough transactions.**</span></span> <span data-ttu-id="221aa-121">Í þessu tilfelli geturðu annaðhvort beðið eftir að fleiri færslur eigi sér stað, uppfært sjálfgefna færibreytur tillögulistans eða notað handvirkar íhlutanir til að breyta tillöguniðurstöðum afurðalista.</span><span class="sxs-lookup"><span data-stu-id="221aa-121">In this case, you can either wait for more transactions to occur, update the default recommendation list parameters, or use manual intervention to modify the recommendation product list results.</span></span> <span data-ttu-id="221aa-122">Fyrir frekari upplýsingar um breytur ráðlegginga, sjá [Stjórna AI-ML byggðum afurðum meðmæla](modify-product-recommendation-results.md).</span><span class="sxs-lookup"><span data-stu-id="221aa-122">For more information about recommendation parameters, see [Manage AI-ML-based product recommendation results](modify-product-recommendation-results.md).</span></span>
1. <span data-ttu-id="221aa-123">**Gakktu úr skugga um að varan uppfylli tillöguviðmið fyrir listann.**</span><span class="sxs-lookup"><span data-stu-id="221aa-123">**Make sure that the product meets the recommendation criteria for the list.**</span></span> <span data-ttu-id="221aa-124">Fyrir frekari upplýsingar um tillögufæribreytur afurða, sjá [Stjórna AI-ML-byggðum niðurstöðum afurðatillagna](modify-product-recommendation-results.md).</span><span class="sxs-lookup"><span data-stu-id="221aa-124">For more information about product recommendation parameters, see [Manage AI-ML-based product recommendation results](modify-product-recommendation-results.md).</span></span>

## <a name="how-can-i-prevent-poor-recommendation-results-from-being-returned"></a><span data-ttu-id="221aa-125">Hvernig get ég komið í veg fyrir að slæmum tillögum sé skilað?</span><span class="sxs-lookup"><span data-stu-id="221aa-125">How can I prevent poor recommendation results from being returned?</span></span>

<span data-ttu-id="221aa-126">Tillögulistar þurfa mikið magn færslna til að skila niðurstöðum.</span><span class="sxs-lookup"><span data-stu-id="221aa-126">Recommendation lists require a large volume of transactions to produce results.</span></span> <span data-ttu-id="221aa-127">Þess vegna er mikilvægt að notendur leggi fram öll söguleg færslugögn.</span><span class="sxs-lookup"><span data-stu-id="221aa-127">Therefore, it's important that users provide full historical transaction data.</span></span>

<span data-ttu-id="221aa-128">Að auki eru afurðir sem hafa engar færslur eða fáar færslur yfirleitt ekki með niðurstöðurnar **Fólki líkar líka** eða **Oft keypt saman** og birtast ekki á tillögulistanum **Vinsælt** eða **Mest selt**.</span><span class="sxs-lookup"><span data-stu-id="221aa-128">Additionally, products that have no transactions or few transactions typically don't have **People also like** or **Frequently bought together** results, and don't appear in **Trending** or **Best selling** recommendation lists.</span></span> <span data-ttu-id="221aa-129">Þessar aðstæður geta oft komið upp fyrir mjög nýjar vörur, eða fyrir gamlar vörur sem eru með lítinn fjölda kaupa.</span><span class="sxs-lookup"><span data-stu-id="221aa-129">This situation can often occur for very new products, or for old products that have a small number of purchases.</span></span> <span data-ttu-id="221aa-130">Vinsælir nýir hlutir munu auðveldlega komast yfir þetta mál.</span><span class="sxs-lookup"><span data-stu-id="221aa-130">Popular new items will easily overcome this issue.</span></span>

<span data-ttu-id="221aa-131">Við mælum með að þú fylgir þessum skrefum:</span><span class="sxs-lookup"><span data-stu-id="221aa-131">We recommend that you follow these steps:</span></span>
1. <span data-ttu-id="221aa-132">**Gakktu úr skugga um að varan uppfylli tillöguviðmið fyrir listann.**</span><span class="sxs-lookup"><span data-stu-id="221aa-132">**Make sure that the product meets the recommendation criteria for that list.**</span></span> <span data-ttu-id="221aa-133">Fyrir frekari upplýsingar um tillögufæribreytur afurða, sjá Breyta AI-ML-byggðum niðurstöðum afurðatillagna.</span><span class="sxs-lookup"><span data-stu-id="221aa-133">For more information about product recommendation parameters, see Modify AI-ML-based product recommendation results.</span></span>
1. <span data-ttu-id="221aa-134">**Ef varan er ný skaltu íhuga að breyta meðmælalistanum þar til varan er komin með fleiri færslur.**</span><span class="sxs-lookup"><span data-stu-id="221aa-134">**If the product is new, consider modifying a recommendation list until the product has more transactions.**</span></span> <span data-ttu-id="221aa-135">Fyrir frekari upplýsingar um hvernig eigi að breyta niðurstöðum tillögulista, sjá [Stjórna AI-ML-byggðum niðurstöðum afurðatillagna](modify-product-recommendation-results.md).</span><span class="sxs-lookup"><span data-stu-id="221aa-135">For more information about how to modify recommendation list results, see [Manage AI-ML-based product recommendation results](modify-product-recommendation-results.md).</span></span>


- <span data-ttu-id="221aa-136">**Gakktu úr skugga um að varan uppfylli tillöguviðmið fyrir listann.**</span><span class="sxs-lookup"><span data-stu-id="221aa-136">**Make sure that the product meets the recommendation criteria for that list.**</span></span> <span data-ttu-id="221aa-137">Fyrir frekari upplýsingar um tillögufæribreytur afurða, sjá [Stjórna AI-ML-byggðum niðurstöðum afurðatillagna](modify-product-recommendation-results.md).</span><span class="sxs-lookup"><span data-stu-id="221aa-137">For more information about product recommendation parameters, see [Manage AI-ML-based product recommendation results](modify-product-recommendation-results.md).</span></span>
- <span data-ttu-id="221aa-138">**Ef varan er ný skaltu íhuga að breyta meðmælalistanum þar til varan er komin með fleiri færslur**.</span><span class="sxs-lookup"><span data-stu-id="221aa-138">**If the product is new, consider modifying a recommendation list until the product has more transactions**.</span></span> <span data-ttu-id="221aa-139">Fyrir frekari upplýsingar um hvernig eigi að breyta niðurstöðum tillögulista, sjá [Stjórna AI-ML-byggðum niðurstöðum afurðatillagna](modify-product-recommendation-results.md).</span><span class="sxs-lookup"><span data-stu-id="221aa-139">For more information about how to modify recommendation list results, see [Manage AI-ML-based product recommendation results](modify-product-recommendation-results.md).</span></span>

## <a name="can-i-remove-a-product-but-still-see-it-in-the-store"></a><span data-ttu-id="221aa-140">Get ég fjarlægt vöru en samt séð hana í versluninni?</span><span class="sxs-lookup"><span data-stu-id="221aa-140">Can I remove a product but still see it in the store?</span></span>

<span data-ttu-id="221aa-141">Þú getur aðlagað lista sem eru búnir til á reiknirit ef viðskiptaþörf kemur upp.</span><span class="sxs-lookup"><span data-stu-id="221aa-141">You can adjust lists that are algorithmically generated if a business need arises.</span></span> <span data-ttu-id="221aa-142">Hins vegar, ef vara er fjarlægð af tillögulistanum, verður varan áfram sýnileg í versluninni.</span><span class="sxs-lookup"><span data-stu-id="221aa-142">However, if a product is removed from a recommendation list, the product will remain discoverable in the store.</span></span> <span data-ttu-id="221aa-143">Fyrir frekari upplýsingar um hvernig eigi að breyta niðurstöðum afurðatillagna, sjá [Stjórna AI-ML-byggðum niðurstöðum afurðatillagna](modify-product-recommendation-results.md).</span><span class="sxs-lookup"><span data-stu-id="221aa-143">For more information about how to modify product recommendation results, see [Manage AI-ML-based product recommendation results](modify-product-recommendation-results.md).</span></span>

<span data-ttu-id="221aa-144">Ef þú verður að hindra að hlutur verði uppgötvaður í versluninni, verður þú að breyta gildinu **Vöruúrval** í **Útiloka**.</span><span class="sxs-lookup"><span data-stu-id="221aa-144">If you must block an item from being discovered in the store, you must change the **Item assortments** value to **Exclude**.</span></span>

## <a name="how-do-i-add-a-list-to-an-e-commerce-page"></a><span data-ttu-id="221aa-145">Hvernig bæti ég lista við netverslunarsíðu?</span><span class="sxs-lookup"><span data-stu-id="221aa-145">How do I add a list to an e-Commerce page?</span></span>

<span data-ttu-id="221aa-146">Nánari upplýsingar um hvernig á að bæta við afurðatillögusíðum við vefverslunina þína, sjá [Bæta afurðatillögulistum við síður](add-reco-list-to-page.md).</span><span class="sxs-lookup"><span data-stu-id="221aa-146">For information about how to add product recommendation pages to your e-Commerce website, see [Add product recommendation lists to pages](add-reco-list-to-page.md).</span></span>

## <a name="how-do-i-enable-recommendations-on-pos"></a><span data-ttu-id="221aa-147">Hvernig get ég virkjað tillögur fyrir POS?</span><span class="sxs-lookup"><span data-stu-id="221aa-147">How do I enable recommendations on POS?</span></span>

<span data-ttu-id="221aa-148">Eftir að hafa gert afurðatillögur virkar þarftu að bæta við tillöguborðinu á POS skjánum.</span><span class="sxs-lookup"><span data-stu-id="221aa-148">After enabling product recommendations, you will need to add the recommendations panel to the control POS screen.</span></span> <span data-ttu-id="221aa-149">Nánari upplýsingar er að finna í [Bæta við tillögustýringu á færsluskjá tækja á sölustað](add-recommendations-control-pos-screen.md).</span><span class="sxs-lookup"><span data-stu-id="221aa-149">For more information, see [Add a recommendations control to the transaction screen on POS devices](add-recommendations-control-pos-screen.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="221aa-150">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="221aa-150">Additional resources</span></span>

[<span data-ttu-id="221aa-151">Yfirlit yfir afurðarráðleggingar</span><span class="sxs-lookup"><span data-stu-id="221aa-151">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="221aa-152">Virkja Azure Data Lake Storage í Dynamics 365 Commerce-umhverfi</span><span class="sxs-lookup"><span data-stu-id="221aa-152">Enable Azure Data Lake Storage in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="221aa-153">Virkja ráðleggingar um afurðir</span><span class="sxs-lookup"><span data-stu-id="221aa-153">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="221aa-154">Kveikja á sérsniðnum tillögum</span><span class="sxs-lookup"><span data-stu-id="221aa-154">Enable personalized recommendations</span></span>](personalized-recommendations.md)

[<span data-ttu-id="221aa-155">Afþakka sérsniðnar tillögur</span><span class="sxs-lookup"><span data-stu-id="221aa-155">Opt out of personalized recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="221aa-156">Bæta afurðaráðleggingum við sölustað</span><span class="sxs-lookup"><span data-stu-id="221aa-156">Add product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="221aa-157">Bæta við tillögum á færsluskjáinn</span><span class="sxs-lookup"><span data-stu-id="221aa-157">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="221aa-158">Aðlagaðu niðurstöður AI-ML</span><span class="sxs-lookup"><span data-stu-id="221aa-158">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="221aa-159">Búðu til handvirkt myndaðar ráðleggingar</span><span class="sxs-lookup"><span data-stu-id="221aa-159">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="221aa-160">Búðu til tillögur með kynningargögnum</span><span class="sxs-lookup"><span data-stu-id="221aa-160">Create recommendations with demo data</span></span>](product-recommendations-demo-data.md)
