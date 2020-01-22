---
title: Upplýsingar um kynningu á kynningu á afurðarásum
description: Þetta skjal miðar að því að veita leiðbeiningar um hvernig skuldsetja megi ráðleggingar um omni-rás vöru í Tier-1 umhverfi með einum reit með því að nota fyrirfram byggðar, sérhannaðar kynningargögn.
author: bebeale
manager: AnnBe
ms.date: 12/1/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-07-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 31aa5dbd2fa814fd572024a4ae36b9d9b46a2fb0
ms.sourcegitcommit: 398c0652acde12c953de007d06055456d6e0a516
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/02/2019
ms.locfileid: "2872327"
---
# <a name="omni-channel-product-recommendations-demo-data"></a><span data-ttu-id="837ad-103">Upplýsingar um kynningu á kynningu á afurðarásum</span><span class="sxs-lookup"><span data-stu-id="837ad-103">Omni-channel product recommendations demo data</span></span>

<span data-ttu-id="837ad-104">Þetta skjal miðar að því að veita leiðbeiningar um hvernig skuldsetja megi ráðleggingar um omni-rás vöru í Tier-1 umhverfi með einum reit með því að nota fyrirfram byggðar, sérhannaðar kynningargögn.</span><span class="sxs-lookup"><span data-stu-id="837ad-104">This document aims to provide guidance on how to leverage omni-channel product recommendations in Tier-1 single box environments using pre-populated, customizable demo data.</span></span>

<span data-ttu-id="837ad-105">Ráðleggingar með Omni-rásum bjóða upp á safn ritstjóralista eða forritaðs myndaðs lista yfir vörur.</span><span class="sxs-lookup"><span data-stu-id="837ad-105">Omni-channel product recommendations provide a set of editorially curated or programmatically generated ordered list of products.</span></span> <span data-ttu-id="837ad-106">Hægt er að nota þessa lista í nokkrum tilfellum, allt eftir viðskiptaþörf.</span><span class="sxs-lookup"><span data-stu-id="837ad-106">These lists can be used in several scenarios, depending on the business need.</span></span> <span data-ttu-id="837ad-107">Nánari upplýsingar um ráðleggingarlista vöru er að finna í [yfirliti yfir ráðleggingar um vörur í POS-skjölum.](../commerce/product-recommendations.md)</span><span class="sxs-lookup"><span data-stu-id="837ad-107">For more information about product recommendation lists, see [Product recommendations overview.](../commerce/product-recommendations.md)</span></span>

<span data-ttu-id="837ad-108">Fyrir Tier-2 og hærra Dynamics Environments eru ráðleggingar sjálfkrafa reiknaðar út frá gögnum viðskiptavina.</span><span class="sxs-lookup"><span data-stu-id="837ad-108">For Tier-2 and higher Dynamics Environments product recommendations are automatically computed based on customer data.</span></span>
<span data-ttu-id="837ad-109">Með því að nota kynningargögn um vörur er ekki gert ráð fyrir neinum lausnum sem hafa þegar verið veittar í umhverfinu og kostnaði sem tengist notkun þeirra.</span><span class="sxs-lookup"><span data-stu-id="837ad-109">Using product recommendations demo data does not disable any product recommendations solution already provisioned in the environment and any costs associated with its usage.</span></span>

<span data-ttu-id="837ad-110">Fyrir Tier-1 umhverfi eru tillögur vöru byggðar eingöngu á stöðluðum kynningu gagna sem geymd eru í csv skrá.</span><span class="sxs-lookup"><span data-stu-id="837ad-110">For Tier-1 environments product recommendations are based only off the static demo data stored in a csv file.</span></span>

## <a name="enabling-product-recommendations-demo-data-in-an-environment"></a><span data-ttu-id="837ad-111">Kveikir á kynningu gagna um kynningu í umhverfi</span><span class="sxs-lookup"><span data-stu-id="837ad-111">Enabling product recommendations demo data in an environment</span></span>

<span data-ttu-id="837ad-112">Viðskiptavinir þurfa að dreifa **Dynamics 365 Commerce Forskoða framlengingu á kynningu** í viðkomandi umhverfi, sem gerir sjálfkrafa kynningu á vöruupplýsingum kynningu gagna.</span><span class="sxs-lookup"><span data-stu-id="837ad-112">Customers need to deploy the **Dynamics 365 Commerce Preview Demo Extension** to the respective environment, which automatically enables product recommendations demo data.</span></span>

## <a name="default-demo-data"></a><span data-ttu-id="837ad-113">Sjálfgefin sýndargögn</span><span class="sxs-lookup"><span data-stu-id="837ad-113">Default demo data</span></span>
<span data-ttu-id="837ad-114">Hvert umhverfi gerð Onebox er með forhlaðnum safni af kynningum um vöruafmæli sem eru geymd í dái sem aðskilin eru **'reco_demo_data.csv'** skrá, sem er staðsett í sömu möppu og þetta skjal á smásöluþjóninum.</span><span class="sxs-lookup"><span data-stu-id="837ad-114">Each Onebox type environment comes with a preloaded set of product recommendations demo data stored in the coma separated **‘reco_demo_data.csv’** file, located in the same folder as this document on Retail Server.</span></span>

<span data-ttu-id="837ad-115">Þessi gögn eru byggð upp meðfram eftirfarandi dálkum</span><span class="sxs-lookup"><span data-stu-id="837ad-115">This data is structured along the following columns</span></span>

| <span data-ttu-id="837ad-116">Dálkheiti</span><span class="sxs-lookup"><span data-stu-id="837ad-116">Column name</span></span>         | <span data-ttu-id="837ad-117">Skylda</span><span class="sxs-lookup"><span data-stu-id="837ad-117">Mandatory</span></span>          | <span data-ttu-id="837ad-118">Lýsing</span><span class="sxs-lookup"><span data-stu-id="837ad-118">Description</span></span>                                                                                                                                 | <span data-ttu-id="837ad-119">Möguleg gildi</span><span class="sxs-lookup"><span data-stu-id="837ad-119">Possible Values</span></span>                                                              |
|---------------------|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="837ad-120">RecoList</span><span class="sxs-lookup"><span data-stu-id="837ad-120">RecoList</span></span>            | :heavy_check_mark: | <span data-ttu-id="837ad-122">Sértæk tegund vöru tilmæla listans sem kynningargagnapunkturinn er að búa til.</span><span class="sxs-lookup"><span data-stu-id="837ad-122">The specific product   recommendation list type that the demo data point is to generate.</span></span>                                                    | <ul><li><span data-ttu-id="837ad-123">RecoBestSelling</span><span class="sxs-lookup"><span data-stu-id="837ad-123">RecoBestSelling</span></span></li><li><span data-ttu-id="837ad-124">RecoNew</span><span class="sxs-lookup"><span data-stu-id="837ad-124">RecoNew</span></span></li><li><span data-ttu-id="837ad-125">RecoTrending</span><span class="sxs-lookup"><span data-stu-id="837ad-125">RecoTrending</span></span></li><li><span data-ttu-id="837ad-126">RecoCart</span><span class="sxs-lookup"><span data-stu-id="837ad-126">RecoCart</span></span></li><li><span data-ttu-id="837ad-127">RecoPeopleAlsoBuy</span><span class="sxs-lookup"><span data-stu-id="837ad-127">RecoPeopleAlsoBuy</span></span></li></ul> |
| <span data-ttu-id="837ad-128">OperatingUnitNumber</span><span class="sxs-lookup"><span data-stu-id="837ad-128">OperatingUnitNumber</span></span> | :heavy_check_mark: | <span data-ttu-id="837ad-130">Sértækt númer rekstrareiningarinnar þar sem gert er ráð fyrir að yfirborð vöru tilmæli komi upp.</span><span class="sxs-lookup"><span data-stu-id="837ad-130">The specific   operating unit number where product recommendations are expected to be   surfaced in.</span></span>                                        |                                                                              |
| <span data-ttu-id="837ad-131">Tegund</span><span class="sxs-lookup"><span data-stu-id="837ad-131">Category</span></span>            |                    |    <span data-ttu-id="837ad-132">Skila skal flokknum fyrir viðkomandi lista.</span><span class="sxs-lookup"><span data-stu-id="837ad-132">The category the   specific list should be returned for.</span></span> <span data-ttu-id="837ad-133">Ef enginn flokkur er tilgreindur er listinn aðeins efst í stýriveldi.</span><span class="sxs-lookup"><span data-stu-id="837ad-133">If no category is specified, list is   for top of navigation hierarchy only.</span></span>    |                                                                              |
| <span data-ttu-id="837ad-134">SeedItemId</span><span class="sxs-lookup"><span data-stu-id="837ad-134">SeedItemId</span></span>          |                    |    <span data-ttu-id="837ad-135">Fyrir lista sem þurfa fræ (RecoPeopleAlsoBuy og RecoCart) vöruna sem listarnir ættu að sýna viðbótarafurðir fyrir.</span><span class="sxs-lookup"><span data-stu-id="837ad-135">For lists that   require seed (RecoPeopleAlsoBuy and RecoCart) the product those lists should   show additional products for.</span></span>            |                                                                              |
| <span data-ttu-id="837ad-136">ItemIds</span><span class="sxs-lookup"><span data-stu-id="837ad-136">ItemIds</span></span>             | :heavy_check_mark: | <span data-ttu-id="837ad-138">Ein eða fleiri vörur sem á að skila í kjölfarið, aðskilin með **';'**.</span><span class="sxs-lookup"><span data-stu-id="837ad-138">One or more products   to be returned as the result, separated by **‘;’**.</span></span>                                                                  |                                                                              |


## <a name="customize-demo-data"></a><span data-ttu-id="837ad-139">Sérsníða sýndargögn</span><span class="sxs-lookup"><span data-stu-id="837ad-139">Customize demo data</span></span>
<span data-ttu-id="837ad-140">Viðskiptavinir geta breytt sjálfgefnum kynningargögnum með hvaða vöru- og flokkaupplýsingum sem eru stilltar í HQ.</span><span class="sxs-lookup"><span data-stu-id="837ad-140">Customers can edit the default demo data with any product and category information that is configured in HQ.</span></span> <span data-ttu-id="837ad-141">Þegar búið er að uppfæra CSV endurspegla vörutillögurnar sem eru sendar til viðskiptavina strax breytingarnar.</span><span class="sxs-lookup"><span data-stu-id="837ad-141">Once the CSV is updated, the Product Recommendations returned to customers will immediately reflect the changes.</span></span>

<span data-ttu-id="837ad-142">Viðbyggingin hefur að geyma gagnapakka sem kallast RecoMockDataset.csv sem gerir viðskiptavininum kleift að stjórna gagnapakkanum sem er notað til að knýja fram niðurstöður ráðlegginga um spotta.</span><span class="sxs-lookup"><span data-stu-id="837ad-142">The extension contains a datafile called RecoMockDataset.csv which allows the customer to control the dataset used to power the mock recommendations results.</span></span> <span data-ttu-id="837ad-143">Hægt er að stjórna skráarheitinu með viðbótarstillingum með því að nota stillinguna **ext.Recommendations.DemoFilePath**.</span><span class="sxs-lookup"><span data-stu-id="837ad-143">The file name can be controlled through extension configuration using the **ext.Recommendations.DemoFilePath** setting.</span></span> <span data-ttu-id="837ad-144">Þetta gerir viðskiptavinum kleift að hafa mörg gagnapakkar tiltækar sem auðvelt er að skipta á milli í gegnum stillingar.</span><span class="sxs-lookup"><span data-stu-id="837ad-144">This enables the customers to have multiple datasets available that can be switched between easily through configuration.</span></span>

```
  <settings>
    <add name="ext.Recommendations.DemoFilePath" value="RecoMockDataset.csv" />
  </settings>
```

## <a name="additional-resources"></a><span data-ttu-id="837ad-145">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="837ad-145">Additional resources</span></span>

[<span data-ttu-id="837ad-146">yfirlit yfir ráðleggingar um afurðir</span><span class="sxs-lookup"><span data-stu-id="837ad-146">Product recommendations overview</span></span>](../commerce/product-recommendations.md)

[<span data-ttu-id="837ad-147">Umhverfisskipulagning</span><span class="sxs-lookup"><span data-stu-id="837ad-147">Environment planning</span></span>](../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md)
