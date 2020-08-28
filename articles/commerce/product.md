---
title: Bæta afurðaráðleggingum við sölustað
description: Þetta efni lýsir notkun ráðlegginga um vöru á sölustað (POS) tæki.
author: bebeale
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 259664
ms.assetid: 5dd8db08-cd96-4f7e-9e65-b05ca815d580
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 7afe9225b8fc966ca154a5eb7421e8d4cc7c3023
ms.sourcegitcommit: 8905d7a7a010e451c5435086480f66650ec54926
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/06/2020
ms.locfileid: "3664835"
---
# <a name="add-product-recommendations-on-pos"></a><span data-ttu-id="1ffb3-103">Bæta afurðaráðleggingum við sölustað</span><span class="sxs-lookup"><span data-stu-id="1ffb3-103">Add product recommendations on POS</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="1ffb3-104">Í kjarna þess eru tillögur vöru umbreytandi viðskiptaumsóknar sem spannar öll viðskiptarými til að skapa ríka, grípandi og sérsniðna vöruuppgötvun.</span><span class="sxs-lookup"><span data-stu-id="1ffb3-104">At its core, product recommendations are a transformative business application that span across all commerce spaces to create rich, engaging, and tailored product discovery experiences.</span></span> <span data-ttu-id="1ffb3-105">Fylgdu skrefunum til að framkvæma þennan eiginleika í POS [hvernig á að bæta ráðleggingum við POS tækin þín.](add-recommendations-control-pos-screen.md)</span><span class="sxs-lookup"><span data-stu-id="1ffb3-105">To implement this feature on POS, follow the steps on [how to add recommendations to your POS devices.](add-recommendations-control-pos-screen.md)</span></span> 

<span data-ttu-id="1ffb3-106">Nánari upplýsingar um ráðleggingareiginleika vöru er að finna í [yfirliti yfir ráðleggingar um vörur í POS-skjölum.](../commerce/product-recommendations.md)</span><span class="sxs-lookup"><span data-stu-id="1ffb3-106">For more information about product recommendations features, read the [product recommendations overview.](../commerce/product-recommendations.md)</span></span> 

## <a name="scenarios"></a><span data-ttu-id="1ffb3-107">Sviðsmyndir</span><span class="sxs-lookup"><span data-stu-id="1ffb3-107">Scenarios</span></span>

<span data-ttu-id="1ffb3-108">Vöruráðleggingar eru virkjaðar fyrir eftirfarandi aðstæður sölustaðar.</span><span class="sxs-lookup"><span data-stu-id="1ffb3-108">Product recommendations are enabled for the following POS scenarios.</span></span> <span data-ttu-id="1ffb3-109">Þær eru tiltækar í sölukerfi í skýinu eða Modern POS (MPOS).</span><span class="sxs-lookup"><span data-stu-id="1ffb3-109">They are available in Cloud POS or Modern POS (MPOS).</span></span>

1. <span data-ttu-id="1ffb3-110">Á síðunni **Upplýsingar um afurð**:</span><span class="sxs-lookup"><span data-stu-id="1ffb3-110">On the **Product details** page:</span></span>

    - <span data-ttu-id="1ffb3-111">Ef aðili tengdur verslun fer á síðuna **Upplýsingar um afurð** þegar hann skoðar fyrri færslur þvert á mismunandi rásir stingur þjónustan upp á fleiri vörum sem eru líklegar til að vera keyptar saman.</span><span class="sxs-lookup"><span data-stu-id="1ffb3-111">If a store associate visits a **Product details** page when looking at previous transactions across different channels, the recommendations service suggests additional items that are likely to be purchased together.</span></span>

    <span data-ttu-id="1ffb3-112">[![Meðmæli á upplýsingasíðu afurðar](./media/proddetails.png)](./media/proddetails.png)</span><span class="sxs-lookup"><span data-stu-id="1ffb3-112">[![Recommendations on the Product details page](./media/proddetails.png)](./media/proddetails.png)</span></span>

2. <span data-ttu-id="1ffb3-113">Á síðunni **Færsla**:</span><span class="sxs-lookup"><span data-stu-id="1ffb3-113">On the **Transaction** page:</span></span>

    - <span data-ttu-id="1ffb3-114">Ráðgjafarvélin leggur til hluti sem byggja á öllum listanum yfir hluti í körfunni sem oft eru keyptir saman.</span><span class="sxs-lookup"><span data-stu-id="1ffb3-114">The recommendation engine suggests items based on the entire list of items in the basket that are frequently bought together.</span></span>

    > [!NOTE]
    > <span data-ttu-id="1ffb3-115">Til að birta ráðleggingar á síðunni **Færsla** þarf smásöluaðilinn að uppfæra skjáútlitið í Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="1ffb3-115">To display recommendations on the **Transaction** page, the retailer needs to update the screen layout in Dynamics 365 Commerce.</span></span> <span data-ttu-id="1ffb3-116">Sleppa verður stýringunni **Ráðleggingar** á síðuna **Færsla**.</span><span class="sxs-lookup"><span data-stu-id="1ffb3-116">The **Recommendations** control must be dropped onto the **Transaction** page.</span></span>

    <span data-ttu-id="1ffb3-117">[![Meðmæli á færslusíðunni](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)</span><span class="sxs-lookup"><span data-stu-id="1ffb3-117">[![Recommendations on the Transaction page](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)</span></span>

## <a name="configure-commerce-to-enable-pos-recommendations"></a><span data-ttu-id="1ffb3-118">Skilgreina Commerce til að virkja ráðleggingar sölustaðar</span><span class="sxs-lookup"><span data-stu-id="1ffb3-118">Configure Commerce to enable POS recommendations</span></span>

<span data-ttu-id="1ffb3-119">Til að setja upp vöruráðleggingar skal fylgja þessum skrefum:</span><span class="sxs-lookup"><span data-stu-id="1ffb3-119">To set up product recommendations, follow these steps:</span></span>

1. <span data-ttu-id="1ffb3-120">Gakktu úr skugga um að þjónusta þín hafi verið uppfærð í **10.0.6 bygging.**</span><span class="sxs-lookup"><span data-stu-id="1ffb3-120">Ensure your service has been updated to the **10.0.6 build.**</span></span>
2. <span data-ttu-id="1ffb3-121">Fylgdu leiðbeiningunum um hvernig á að gera [virkja tillögur um vöru](../commerce/enable-product-recommendations.md) fyrir fyrirtæki þitt.</span><span class="sxs-lookup"><span data-stu-id="1ffb3-121">Follow the instructions on how to [enable product recommendations](../commerce/enable-product-recommendations.md) for your business.</span></span>
3. <span data-ttu-id="1ffb3-122">Valfrjálst: Til Að birta ráðleggingar á færsluskjánum, er farið í **Útlit Skjás**útlit skjás valið **Útlitshönnuður afgreiðsluskjás** opnaður, og svo sleppt stýringunni **leiðbeiningar** þar sem þarf.</span><span class="sxs-lookup"><span data-stu-id="1ffb3-122">Optional: To display recommendations on the transaction screen, go to **Screen Layout**, choose your screen layout, launch the **Screen layout designer**, and then drop the **recommendations** control where needed.</span></span>
4. <span data-ttu-id="1ffb3-123">Farið í **Færibreytur Commerce**, veljið **Vélnám** svo **Já** undir **virkja ráðleggingar sölustaðar**.</span><span class="sxs-lookup"><span data-stu-id="1ffb3-123">Go to **Commerce parameters**, select **Machine-learning**, select **Yes** under **Enable POS recommendations**.</span></span>
5. <span data-ttu-id="1ffb3-124">Til að sjá ráðleggingar á sölustað skal keyra altæku vinnsluna **1110**.</span><span class="sxs-lookup"><span data-stu-id="1ffb3-124">To see recommendations on POS, run global configuration job **1110**.</span></span> <span data-ttu-id="1ffb3-125">Til að endurspegla breytingar á útlitshönnuði sölustaðar skal keyra skilgreiningarvinnslu rásar **1070**.</span><span class="sxs-lookup"><span data-stu-id="1ffb3-125">To reflect changes made to POS screen layout designer, run channel configuration job **1070**.</span></span>

## <a name="troubleshoot-issues-where-you-have-product-recommendations-already-enabled"></a><span data-ttu-id="1ffb3-126">Finna úrræði á vandamálum þar sem ráðleggingar um vörur hafa þegar verið virkjaðar</span><span class="sxs-lookup"><span data-stu-id="1ffb3-126">Troubleshoot issues where you have Product recommendations already enabled</span></span>

- <span data-ttu-id="1ffb3-127">Flettið upp á **Færibreytur Commerce** \> **Ráðleggingalistar** \> **Slökkva á ráðleggingum um vörur** og keyrið **Altæka skilgreiningarvinnslu \[9999\]**.</span><span class="sxs-lookup"><span data-stu-id="1ffb3-127">Navigate to **Commerce Parameters** \> **Recommendation lists** \> **Disable product recommendations** and run **Global configuration job \[9999\]**.</span></span> 
- <span data-ttu-id="1ffb3-128">Ef **Stýringu ráðleggingar** var bætt við færsluskjáinn með því að nota **Útlitshönnun afgreiðsluskjás** skaltu fjarlægja hana líka.</span><span class="sxs-lookup"><span data-stu-id="1ffb3-128">If you added the **Recommendations control** to your transaction screen using the **Screen layout designer**, please remove that as well.</span></span>
- <span data-ttu-id="1ffb3-129">Ef þú hefur frekari spurningar skaltu skoða [Algengar spurningar um afurðaráðleggingar](../commerce/faq-recommendations.md) fyrir meiri upplýsingar.</span><span class="sxs-lookup"><span data-stu-id="1ffb3-129">If you have additional questions, check out the [Product recommendations FAQ](../commerce/faq-recommendations.md) for more information.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="1ffb3-130">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="1ffb3-130">Additional resources</span></span>

[<span data-ttu-id="1ffb3-131">Yfirlit yfir afurðarráðleggingar</span><span class="sxs-lookup"><span data-stu-id="1ffb3-131">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="1ffb3-132">Virkja Azure Data Lake Storage í Dynamics 365 Commerce-umhverfi</span><span class="sxs-lookup"><span data-stu-id="1ffb3-132">Enable Azure Data Lake Storage in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="1ffb3-133">Virkja ráðleggingar um afurðir</span><span class="sxs-lookup"><span data-stu-id="1ffb3-133">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="1ffb3-134">Kveikja á sérsniðnum tillögum</span><span class="sxs-lookup"><span data-stu-id="1ffb3-134">Enable personalized recommendations</span></span>](personalized-recommendations.md)

[<span data-ttu-id="1ffb3-135">Afþakka sérsniðnar tillögur</span><span class="sxs-lookup"><span data-stu-id="1ffb3-135">Opt out of personalized recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="1ffb3-136">Virkja tillögur um að kaupa svipaða vöru</span><span class="sxs-lookup"><span data-stu-id="1ffb3-136">Enable "shop similar looks" recommendations</span></span>](shop-similar-looks.md)

[<span data-ttu-id="1ffb3-137">Bæta tillögum við færsluskjáinn</span><span class="sxs-lookup"><span data-stu-id="1ffb3-137">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="1ffb3-138">Aðlagaðu niðurstöður AI-ML</span><span class="sxs-lookup"><span data-stu-id="1ffb3-138">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="1ffb3-139">Búðu til handvirkt myndaðar ráðleggingar</span><span class="sxs-lookup"><span data-stu-id="1ffb3-139">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="1ffb3-140">Búðu til tillögur með kynningargögnum</span><span class="sxs-lookup"><span data-stu-id="1ffb3-140">Create recommendations with demo data</span></span>](product-recommendations-demo-data.md)

[<span data-ttu-id="1ffb3-141">Algengar spurningar um afurðaráðleggingar</span><span class="sxs-lookup"><span data-stu-id="1ffb3-141">Product recommendations FAQ</span></span>](faq-recommendations.md)
