---
title: Fá afurðartillögur með því að nota sýnigögn
description: Þetta skjal veitir leiðbeiningar um hvernig skuldsetja megi ráðleggingar um omni-rás vöru í Tier-1 umhverfi með einum reit með því að nota fyrirfram byggðar, sérhannaðar kynningargögn.
author: bebeale
manager: AnnBe
ms.date: 10/01/19
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
ms.openlocfilehash: 1456feb0665b6ec79a36a3704f17da80ffd759a0
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/12/2020
ms.locfileid: "3042781"
---
# <a name="get-product-recommendations-using-demo-data"></a><span data-ttu-id="cea19-103">Fá afurðartillögur með því að nota sýnigögn</span><span class="sxs-lookup"><span data-stu-id="cea19-103">Get product recommendations using demo data</span></span>
<span data-ttu-id="cea19-104">Þetta skjal veitir leiðbeiningar um hvernig skuldsetja megi ráðleggingar um omni-rás vöru í Tier-1 umhverfi með einum reit með því að nota fyrirfram byggðar, sérhannaðar kynningargögn.</span><span class="sxs-lookup"><span data-stu-id="cea19-104">This document provides guidance on how to leverage omni-channel product recommendations in Tier-1 single box environments using pre-populated, customizable demo data.</span></span>

<span data-ttu-id="cea19-105">Ráðleggingar með Omni-rásum bjóða upp á safn ritstjóralista eða forritaðs myndaðs lista yfir vörur.</span><span class="sxs-lookup"><span data-stu-id="cea19-105">Omni-channel product recommendations provide a set of editorially curated or programmatically generated list of products.</span></span> <span data-ttu-id="cea19-106">Hægt er að nota þessa lista í nokkrum tilfellum, allt eftir viðskiptaþörf.</span><span class="sxs-lookup"><span data-stu-id="cea19-106">These lists can be used in several scenarios, depending on the business need.</span></span> <span data-ttu-id="cea19-107">Nánari upplýsingar um afurðatillögur er að finna í [yfirliti yfir afurðatillögur í POS-skjölum](product-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="cea19-107">For more information about product recommendation lists, see [Product recommendations overview](product-recommendations.md).</span></span>

<span data-ttu-id="cea19-108">Fyrir Tier-2 og hærra umverfi Dynamics 365 eru afurðatillögur sjálfkrafa reiknaðar út frá gögnum viðskiptavina.</span><span class="sxs-lookup"><span data-stu-id="cea19-108">For Tier-2 and higher Dynamics 365 environments, product recommendations are automatically computed based on customer data.</span></span> <span data-ttu-id="cea19-109">Með því að nota kynningargögn um vörur er ekki gert ráð fyrir neinum lausnum sem hafa þegar verið veittar í umhverfinu og kostnaði sem tengist notkun þeirra.</span><span class="sxs-lookup"><span data-stu-id="cea19-109">Using product recommendations demo data does not disable any product recommendations solution already provisioned in the environment and any costs associated with its usage.</span></span>

<span data-ttu-id="cea19-110">Fyrir Tier-1 umhverfi eru afurðatillögur byggðar eingöngu á stöðluðum kynningu gagna sem geymd eru í .csv-skrá.</span><span class="sxs-lookup"><span data-stu-id="cea19-110">For Tier-1 environments, product recommendations are based only off the static demo data stored in a .csv file.</span></span>

## <a name="enabling-product-recommendations-demo-data-in-an-environment"></a><span data-ttu-id="cea19-111">Kveikir á kynningu gagna um kynningu í umhverfi</span><span class="sxs-lookup"><span data-stu-id="cea19-111">Enabling product recommendations demo data in an environment</span></span>
<span data-ttu-id="cea19-112">Til að virkja kynningargögn afurðatillagna þarftu að setja upp Dynamics 365 Commerce Forskoða kynningarviðbót í viðkomandi umhverfi.</span><span class="sxs-lookup"><span data-stu-id="cea19-112">To enable product recommensations demo date, you need to deploy the Dynamics 365 Commerce Preview Demo Extension to the respective environment.</span></span> <span data-ttu-id="cea19-113">Með því að gera það sjálfkrafa er gert ráð fyrir kynningu gagna um afurðatillögur.</span><span class="sxs-lookup"><span data-stu-id="cea19-113">Doing so automatically enables product recommendations demo data.</span></span>

## <a name="default-demo-data"></a><span data-ttu-id="cea19-114">Sjálfgefin sýndargögn</span><span class="sxs-lookup"><span data-stu-id="cea19-114">Default demo data</span></span>
<span data-ttu-id="cea19-115">Hver umhverfisgerð Onebox er með forsóttu safni af kynningargögnum afurðatillagna sem eru geymd í kommuaðskildri 'reco_demo_data.csv' skrá, sem er staðsett í sömu möppu og þetta skjal á Commerce Scale Unit.</span><span class="sxs-lookup"><span data-stu-id="cea19-115">Each Onebox type environment comes with a preloaded set of product recommendations demo data stored in the coma separated ‘reco_demo_data.csv’ file, located on the Commerce Scale Unit.</span></span>

<span data-ttu-id="cea19-116">Gögnin eru byggð upp meðfram eftirfarandi dálkum.</span><span class="sxs-lookup"><span data-stu-id="cea19-116">The data is structured along the following columns.</span></span>

| <span data-ttu-id="cea19-117">Heiti dálks</span><span class="sxs-lookup"><span data-stu-id="cea19-117">Column name</span></span>         | <span data-ttu-id="cea19-118">Skylda</span><span class="sxs-lookup"><span data-stu-id="cea19-118">Mandatory</span></span>          | <span data-ttu-id="cea19-119">Lýsing</span><span class="sxs-lookup"><span data-stu-id="cea19-119">Description</span></span>                                                                                                                                 | <span data-ttu-id="cea19-120">Möguleg gildi</span><span class="sxs-lookup"><span data-stu-id="cea19-120">Possible Values</span></span>                                                              |
|---------------------|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="cea19-121">RecoList</span><span class="sxs-lookup"><span data-stu-id="cea19-121">RecoList</span></span>            | :heavy_check_mark: | <span data-ttu-id="cea19-123">Sú sértæka gerð afurðatilmælalistans sem kynningargagnapunkturinn á að mynda.</span><span class="sxs-lookup"><span data-stu-id="cea19-123">The specific product recommendation list type that the demo data point is to generate.</span></span>                                                    | <ul><li><span data-ttu-id="cea19-124">RecoBestSelling</span><span class="sxs-lookup"><span data-stu-id="cea19-124">RecoBestSelling</span></span></li><li><span data-ttu-id="cea19-125">RecoNew</span><span class="sxs-lookup"><span data-stu-id="cea19-125">RecoNew</span></span></li><li><span data-ttu-id="cea19-126">RecoTrending</span><span class="sxs-lookup"><span data-stu-id="cea19-126">RecoTrending</span></span></li><li><span data-ttu-id="cea19-127">RecoCart</span><span class="sxs-lookup"><span data-stu-id="cea19-127">RecoCart</span></span></li><li><span data-ttu-id="cea19-128">RecoPeopleAlsoBuy</span><span class="sxs-lookup"><span data-stu-id="cea19-128">RecoPeopleAlsoBuy</span></span></li></ul> |
| <span data-ttu-id="cea19-129">OperatingUnitNumber</span><span class="sxs-lookup"><span data-stu-id="cea19-129">OperatingUnitNumber</span></span> | :heavy_check_mark: | <span data-ttu-id="cea19-131">Sértækt númer rekstrareiningarinnar þar sem gert er ráð fyrir að yfirborð vöru tilmæli komi upp.</span><span class="sxs-lookup"><span data-stu-id="cea19-131">The specific operating unit number where product recommendations are expected to be   surfaced.</span></span>                                        |                                                                              |
| <span data-ttu-id="cea19-132">Tegund</span><span class="sxs-lookup"><span data-stu-id="cea19-132">Category</span></span>            |                    |    <span data-ttu-id="cea19-133">Skila skal flokknum fyrir viðkomandi lista.</span><span class="sxs-lookup"><span data-stu-id="cea19-133">The category the specific list should be returned for.</span></span> <span data-ttu-id="cea19-134">Ef enginn flokkur er tilgreindur er listinn aðeins efst í stýriveldi.</span><span class="sxs-lookup"><span data-stu-id="cea19-134">If no category is specified, the list is for top of navigation hierarchy only.</span></span>    |                                                                              |
| <span data-ttu-id="cea19-135">SeedItemId</span><span class="sxs-lookup"><span data-stu-id="cea19-135">SeedItemId</span></span>          |                    |    <span data-ttu-id="cea19-136">Fyrir lista sem þurfa fræ (RecoPeopleAlsoBuy og RecoCart) vöruna sem listarnir ættu að sýna viðbótarafurðir fyrir.</span><span class="sxs-lookup"><span data-stu-id="cea19-136">For lists that require seed (RecoPeopleAlsoBuy and RecoCart), the product those lists should show additional products for.</span></span>            |                                                                              |
| <span data-ttu-id="cea19-137">ItemIds</span><span class="sxs-lookup"><span data-stu-id="cea19-137">ItemIds</span></span>             | :heavy_check_mark: | <span data-ttu-id="cea19-139">Ein eða fleiri vörur sem á að skila í kjölfarið, aðskilin með ';'.</span><span class="sxs-lookup"><span data-stu-id="cea19-139">One or more products to be returned as the result, separated by ‘;’.</span></span>                                                                  |                                                                              |

## <a name="customize-demo-data"></a><span data-ttu-id="cea19-140">Sérsníða sýndargögn</span><span class="sxs-lookup"><span data-stu-id="cea19-140">Customize demo data</span></span>
<span data-ttu-id="cea19-141">Hægt er að breyta sjálfgefnum kynningargögnum með hvaða vöru- og flokkaupplýsingum sem eru stilltar í HQ.</span><span class="sxs-lookup"><span data-stu-id="cea19-141">You can edit the default demo data with any product and category information configured in HQ.</span></span> <span data-ttu-id="cea19-142">Þegar búið er að uppfæra .csv endurspegla afurðatillögurnar sem eru sendar til viðskiptavina strax breytingarnar.</span><span class="sxs-lookup"><span data-stu-id="cea19-142">Once you update the .csv, the product recommendations that are returned to customers will immediately reflect the changes.</span></span>

<span data-ttu-id="cea19-143">Viðbyggingin hefur að geyma gagnapakka sem kallast RecoMockDataset.csv sem gerir þér kleift að stjórna gagnapakkanum sem er notað til að knýja fram niðurstöður ráðlegginga um spotta.</span><span class="sxs-lookup"><span data-stu-id="cea19-143">The extension contains a datafile called 'RecoMockDataset.csv' which allows you to control the dataset used to power the mock recommendations results.</span></span> <span data-ttu-id="cea19-144">Hægt er að stjórna skráarheitinu með viðbótarstillingum með því að nota stillinguna **ext.Recommendations.DemoFilePath**.</span><span class="sxs-lookup"><span data-stu-id="cea19-144">The file name can be controlled through extension configuration using the **ext.Recommendations.DemoFilePath** setting.</span></span> <span data-ttu-id="cea19-145">Þetta gerir þér kleift að hafa mörg gagnapakkar tiltækar sem auðvelt er að skipta á milli í gegnum stillingar.</span><span class="sxs-lookup"><span data-stu-id="cea19-145">This enables you to have multiple datasets available that can be switched between easily through configuration.</span></span>


```xml
<settings>
    <add name="ext.Recommendations.DemoFilePath" value="RecoMockDataset.csv" />
</settings>
```

## <a name="additional-resources"></a><span data-ttu-id="cea19-146">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="cea19-146">Additional Resources</span></span>

[<span data-ttu-id="cea19-147">Yfirlit yfir afurðarráðleggingar</span><span class="sxs-lookup"><span data-stu-id="cea19-147">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="cea19-148">Umhverfisskipulagning</span><span class="sxs-lookup"><span data-stu-id="cea19-148">Environment planning</span></span>](../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md)
