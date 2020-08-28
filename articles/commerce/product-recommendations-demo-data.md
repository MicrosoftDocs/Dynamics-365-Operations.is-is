---
title: Búðu til tillögur með kynningargögnum
description: Þetta efni veitir leiðbeiningar um hvernig skuldsetja megi ráðleggingar um omni-rás vöru í Tier-1 umhverfi með einum reit með því að nota fyrirfram byggðar, sérhannaðar kynningargögn.
author: bebeale
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: RetailStoreTable, RetailTillLayout
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 260624
ms.assetid: a4f9d315-9951-451c-8ee6-37f9b3b15ef0
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: cca6913375eec2565852676f3c1da5a67f71e14f
ms.sourcegitcommit: 8905d7a7a010e451c5435086480f66650ec54926
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/06/2020
ms.locfileid: "3664907"
---
# <a name="create-recommendations-with-demo-data"></a><span data-ttu-id="9bc18-103">Búðu til tillögur með kynningargögnum</span><span class="sxs-lookup"><span data-stu-id="9bc18-103">Create recommendations with demo data</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="9bc18-104">Þetta efni veitir leiðbeiningar um hvernig skuldsetja megi ráðleggingar um omni-rás vöru í Tier-1 umhverfi með einum reit með því að nota fyrirfram byggðar, sérhannaðar kynningargögn.</span><span class="sxs-lookup"><span data-stu-id="9bc18-104">This topic provides guidance on how to leverage omni-channel product recommendations in Tier-1 single box environments using pre-populated, customizable demo data.</span></span>

<span data-ttu-id="9bc18-105">Ráðleggingar með Omni-rásum bjóða upp á safn ritstjóralista eða forritaðs myndaðs lista yfir vörur.</span><span class="sxs-lookup"><span data-stu-id="9bc18-105">Omni-channel product recommendations provide a set of editorially curated or programmatically generated list of products.</span></span> <span data-ttu-id="9bc18-106">Hægt er að nota þessa lista í nokkrum tilfellum, allt eftir viðskiptaþörf.</span><span class="sxs-lookup"><span data-stu-id="9bc18-106">These lists can be used in several scenarios, depending on the business need.</span></span> <span data-ttu-id="9bc18-107">Nánari upplýsingar um afurðatillögur er að finna í [yfirliti yfir afurðatillögur í POS-skjölum](product-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="9bc18-107">For more information about product recommendation lists, see [Product recommendations overview](product-recommendations.md).</span></span>

<span data-ttu-id="9bc18-108">Fyrir Tier-2 og hærra umverfi Dynamics 365 eru afurðatillögur sjálfkrafa reiknaðar út frá gögnum viðskiptavina.</span><span class="sxs-lookup"><span data-stu-id="9bc18-108">For Tier-2 and higher Dynamics 365 environments, product recommendations are automatically computed based on customer data.</span></span> <span data-ttu-id="9bc18-109">Með því að nota kynningargögn um vörur er ekki gert ráð fyrir neinum lausnum sem hafa þegar verið veittar í umhverfinu og kostnaði sem tengist notkun þeirra.</span><span class="sxs-lookup"><span data-stu-id="9bc18-109">Using product recommendations demo data does not disable any product recommendations solution already provisioned in the environment and any costs associated with its usage.</span></span>

<span data-ttu-id="9bc18-110">Fyrir Tier-1 umhverfi eru afurðatillögur byggðar eingöngu á stöðluðum kynningu gagna sem geymd eru í .csv-skrá.</span><span class="sxs-lookup"><span data-stu-id="9bc18-110">For Tier-1 environments, product recommendations are based only off the static demo data stored in a .csv file.</span></span>

## <a name="enabling-product-recommendations-demo-data-in-an-environment"></a><span data-ttu-id="9bc18-111">Kveikir á kynningu gagna um kynningu í umhverfi</span><span class="sxs-lookup"><span data-stu-id="9bc18-111">Enabling product recommendations demo data in an environment</span></span>
<span data-ttu-id="9bc18-112">Til að virkja kynningargögn afurðatillagna þarftu að setja upp Dynamics 365 Commerce Forskoða kynningarviðbót í viðkomandi umhverfi.</span><span class="sxs-lookup"><span data-stu-id="9bc18-112">To enable product recommendations demo date, you need to deploy the Dynamics 365 Commerce Preview Demo Extension to the respective environment.</span></span> <span data-ttu-id="9bc18-113">Með því að gera það sjálfkrafa er gert ráð fyrir kynningu gagna um afurðatillögur.</span><span class="sxs-lookup"><span data-stu-id="9bc18-113">Doing so automatically enables product recommendations demo data.</span></span>

## <a name="default-demo-data"></a><span data-ttu-id="9bc18-114">Sjálfgefin sýndargögn</span><span class="sxs-lookup"><span data-stu-id="9bc18-114">Default demo data</span></span>
<span data-ttu-id="9bc18-115">Hver umhverfisgerð OneBox er með forsóttu safni af kynningargögnum afurðatillagna sem eru geymd í kommuaðskildri 'reco_demo_data.csv' skrá, sem er staðsett í sömu möppu og þetta skjal á Commerce Scale Unit.</span><span class="sxs-lookup"><span data-stu-id="9bc18-115">Each OneBox type environment comes with a preloaded set of product recommendations demo data stored in the coma separated 'reco_demo_data.csv' file, located on the Commerce Scale Unit.</span></span>

<span data-ttu-id="9bc18-116">Gögnin eru byggð upp meðfram eftirfarandi dálkum.</span><span class="sxs-lookup"><span data-stu-id="9bc18-116">The data is structured along the following columns.</span></span>

| <span data-ttu-id="9bc18-117">Dálkheiti</span><span class="sxs-lookup"><span data-stu-id="9bc18-117">Column name</span></span>         | <span data-ttu-id="9bc18-118">Skylda</span><span class="sxs-lookup"><span data-stu-id="9bc18-118">Mandatory</span></span>          | <span data-ttu-id="9bc18-119">lýsing</span><span class="sxs-lookup"><span data-stu-id="9bc18-119">Description</span></span>                                                                                                                                 | <span data-ttu-id="9bc18-120">Möguleg gildi</span><span class="sxs-lookup"><span data-stu-id="9bc18-120">Possible values</span></span>                                                              |
|---------------------|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="9bc18-121">RecoList</span><span class="sxs-lookup"><span data-stu-id="9bc18-121">RecoList</span></span>            | :heavy_check_mark: | <span data-ttu-id="9bc18-123">Sú sértæka gerð afurðatilmælalistans sem kynningargagnapunkturinn á að mynda.</span><span class="sxs-lookup"><span data-stu-id="9bc18-123">The specific product recommendation list type that the demo data point is to generate.</span></span>                                                    | <ul><li><span data-ttu-id="9bc18-124">RecoBestSelling</span><span class="sxs-lookup"><span data-stu-id="9bc18-124">RecoBestSelling</span></span></li><li><span data-ttu-id="9bc18-125">RecoNew</span><span class="sxs-lookup"><span data-stu-id="9bc18-125">RecoNew</span></span></li><li><span data-ttu-id="9bc18-126">RecoTrending</span><span class="sxs-lookup"><span data-stu-id="9bc18-126">RecoTrending</span></span></li><li><span data-ttu-id="9bc18-127">RecoCart</span><span class="sxs-lookup"><span data-stu-id="9bc18-127">RecoCart</span></span></li><li><span data-ttu-id="9bc18-128">RecoPeopleAlsoBuy</span><span class="sxs-lookup"><span data-stu-id="9bc18-128">RecoPeopleAlsoBuy</span></span></li></ul> |
| <span data-ttu-id="9bc18-129">OperatingUnitNumber</span><span class="sxs-lookup"><span data-stu-id="9bc18-129">OperatingUnitNumber</span></span> | :heavy_check_mark: | <span data-ttu-id="9bc18-131">Sértækt númer rekstrareiningarinnar þar sem gert er ráð fyrir að yfirborð vöru tilmæli komi upp.</span><span class="sxs-lookup"><span data-stu-id="9bc18-131">The specific operating unit number where product recommendations are expected to be   surfaced.</span></span>                                        |                                                                              |
| <span data-ttu-id="9bc18-132">Tegund</span><span class="sxs-lookup"><span data-stu-id="9bc18-132">Category</span></span>            |                    |    <span data-ttu-id="9bc18-133">Skila skal flokknum fyrir viðkomandi lista.</span><span class="sxs-lookup"><span data-stu-id="9bc18-133">The category the specific list should be returned for.</span></span> <span data-ttu-id="9bc18-134">Ef enginn flokkur er tilgreindur er listinn aðeins efst í stýriveldi.</span><span class="sxs-lookup"><span data-stu-id="9bc18-134">If no category is specified, the list is for top of navigation hierarchy only.</span></span>    |                                                                              |
| <span data-ttu-id="9bc18-135">SeedItemId</span><span class="sxs-lookup"><span data-stu-id="9bc18-135">SeedItemId</span></span>          |                    |    <span data-ttu-id="9bc18-136">Fyrir lista sem þurfa fræ (RecoPeopleAlsoBuy og RecoCart) vöruna sem listarnir ættu að sýna viðbótarafurðir fyrir.</span><span class="sxs-lookup"><span data-stu-id="9bc18-136">For lists that require seed (RecoPeopleAlsoBuy and RecoCart), the product those lists should show additional products for.</span></span>            |                                                                              |
| <span data-ttu-id="9bc18-137">CustomerId</span><span class="sxs-lookup"><span data-stu-id="9bc18-137">CustomerId</span></span>          |                    |    <span data-ttu-id="9bc18-138">Fyrir lista sem krefjast auðkenni viðskiptavina (RecoPicks).</span><span class="sxs-lookup"><span data-stu-id="9bc18-138">For lists that require a customer identifier (RecoPicks).</span></span>  <span data-ttu-id="9bc18-139">Sjálfgefið gildi '0' á við um alla viðskiptavini.</span><span class="sxs-lookup"><span data-stu-id="9bc18-139">The default value '0' applies to all customers.</span></span>          |                                                                              |
| <span data-ttu-id="9bc18-140">ItemIds</span><span class="sxs-lookup"><span data-stu-id="9bc18-140">ItemIds</span></span>             | :heavy_check_mark: | <span data-ttu-id="9bc18-142">Ein eða fleiri vörur sem á að skila í kjölfarið, aðskilin með ';'.</span><span class="sxs-lookup"><span data-stu-id="9bc18-142">One or more products to be returned as the result, separated by ';'.</span></span>                                                                  |                                                                              |

## <a name="customize-demo-data"></a><span data-ttu-id="9bc18-143">Sérsníða sýndargögn</span><span class="sxs-lookup"><span data-stu-id="9bc18-143">Customize demo data</span></span>
<span data-ttu-id="9bc18-144">Hægt er að breyta sjálfgefnum kynningargögnum með hvaða vöru- og flokkaupplýsingum sem eru stilltar í HQ.</span><span class="sxs-lookup"><span data-stu-id="9bc18-144">You can edit the default demo data with any product and category information configured in HQ.</span></span> <span data-ttu-id="9bc18-145">Þegar búið er að uppfæra .csv endurspegla afurðatillögurnar sem eru sendar til viðskiptavina strax breytingarnar.</span><span class="sxs-lookup"><span data-stu-id="9bc18-145">After you update the .csv, the product recommendations that are returned to customers will immediately reflect the changes.</span></span>

<span data-ttu-id="9bc18-146">Viðbyggingin hefur að geyma gagnapakka sem kallast „RecoMockDataset.csv” sem gerir þér kleift að stjórna gagnapakkanum sem er notað til að knýja fram niðurstöður ráðlegginga um spotta.</span><span class="sxs-lookup"><span data-stu-id="9bc18-146">The extension contains a datafile called 'RecoMockDataset.csv', which allows you to control the dataset used to power the mock recommendations results.</span></span> <span data-ttu-id="9bc18-147">Hægt er að stjórna skráarheitinu með viðbótarstillingum með því að nota stillinguna **ext.Recommendations.DemoFilePath**.</span><span class="sxs-lookup"><span data-stu-id="9bc18-147">The file name can be controlled through extension configuration using the **ext.Recommendations.DemoFilePath** setting.</span></span> <span data-ttu-id="9bc18-148">Þetta gerir þér kleift að hafa mörg gagnapakkar tiltækar sem auðvelt er að skipta á milli í gegnum stillingar.</span><span class="sxs-lookup"><span data-stu-id="9bc18-148">This enables you to have multiple datasets available that can be switched between easily through configuration.</span></span>


```xml
<settings>
    <add name="ext.Recommendations.DemoFilePath" value="RecoMockDataset.csv" />
</settings>
```

## <a name="additional-resources"></a><span data-ttu-id="9bc18-149">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="9bc18-149">Additional resources</span></span>

[<span data-ttu-id="9bc18-150">Yfirlit yfir afurðarráðleggingar</span><span class="sxs-lookup"><span data-stu-id="9bc18-150">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="9bc18-151">Virkja Azure Data Lake Storage í Dynamics 365 Commerce-umhverfi</span><span class="sxs-lookup"><span data-stu-id="9bc18-151">Enable Azure Data Lake Storage in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="9bc18-152">Virkja ráðleggingar um afurðir</span><span class="sxs-lookup"><span data-stu-id="9bc18-152">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="9bc18-153">Kveikja á sérsniðnum tillögum</span><span class="sxs-lookup"><span data-stu-id="9bc18-153">Enable personalized recommendations</span></span>](personalized-recommendations.md)

[<span data-ttu-id="9bc18-154">Afþakka sérsniðnar tillögur</span><span class="sxs-lookup"><span data-stu-id="9bc18-154">Opt out of personalized recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="9bc18-155">Virkja tillögur um að kaupa svipaða vöru</span><span class="sxs-lookup"><span data-stu-id="9bc18-155">Enable "shop similar looks" recommendations</span></span>](shop-similar-looks.md)

[<span data-ttu-id="9bc18-156">Bæta við afurðatillögum á sölustað</span><span class="sxs-lookup"><span data-stu-id="9bc18-156">Add product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="9bc18-157">Bæta tillögum við færsluskjáinn</span><span class="sxs-lookup"><span data-stu-id="9bc18-157">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="9bc18-158">Aðlagaðu niðurstöður AI-ML</span><span class="sxs-lookup"><span data-stu-id="9bc18-158">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="9bc18-159">Búðu til handvirkt myndaðar ráðleggingar</span><span class="sxs-lookup"><span data-stu-id="9bc18-159">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="9bc18-160">Algengar spurningar um afurðaráðleggingar</span><span class="sxs-lookup"><span data-stu-id="9bc18-160">Product recommendations FAQ</span></span>](faq-recommendations.md)
