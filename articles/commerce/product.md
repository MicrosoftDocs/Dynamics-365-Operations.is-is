---
title: Afurðaráðleggingar í POS
description: Þetta efni lýsir notkun ráðlegginga um vöru á sölustað (POS) tæki.
author: bebeale
manager: AnnBe
ms.date: 10/01/19
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
ms.openlocfilehash: bfb13904b774558907b29e74158b1e0a193e17cd
ms.sourcegitcommit: 12b9d6f2dd24e52e46487748c848864909af6967
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/14/2020
ms.locfileid: "3057442"
---
# <a name="product-recommendations-on-pos"></a><span data-ttu-id="672e9-103">Afurðaráðleggingar á sölustað</span><span class="sxs-lookup"><span data-stu-id="672e9-103">Product recommendations on POS</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="672e9-104">Í kjarna þess eru tillögur vöru umbreytandi viðskiptaumsóknar sem spannar öll viðskiptarými til að skapa ríka, grípandi og sérsniðna vöruuppgötvun.</span><span class="sxs-lookup"><span data-stu-id="672e9-104">At its core, product recommendations are a transformative business application that span across all commerce spaces to create rich, engaging, and tailored product discovery experiences.</span></span> <span data-ttu-id="672e9-105">Fylgdu skrefunum til að framkvæma þennan eiginleika í POS [hvernig á að bæta ráðleggingum við POS tækin þín.](add-recommendations-control-pos-screen.md)</span><span class="sxs-lookup"><span data-stu-id="672e9-105">To implement this feature on POS, follow the steps on [how to add recommendations to your POS devices.](add-recommendations-control-pos-screen.md)</span></span> 

<span data-ttu-id="672e9-106">Nánari upplýsingar um ráðleggingareiginleika vöru er að finna í [yfirliti yfir ráðleggingar um vörur í POS-skjölum.](../commerce/product-recommendations.md)</span><span class="sxs-lookup"><span data-stu-id="672e9-106">For more information about product recommendations features, read the [product recommendations overview.](../commerce/product-recommendations.md)</span></span> 

## <a name="scenarios"></a><span data-ttu-id="672e9-107">Sviðsmyndir</span><span class="sxs-lookup"><span data-stu-id="672e9-107">Scenarios</span></span>

<span data-ttu-id="672e9-108">Vöruráðleggingar eru virkjaðar fyrir eftirfarandi aðstæður sölustaðar.</span><span class="sxs-lookup"><span data-stu-id="672e9-108">Product recommendations are enabled for the following POS scenarios.</span></span> <span data-ttu-id="672e9-109">Þær eru tiltækar í sölukerfi í skýinu eða Modern POS (MPOS).</span><span class="sxs-lookup"><span data-stu-id="672e9-109">They are available in Cloud POS or Modern POS (MPOS).</span></span>

1. <span data-ttu-id="672e9-110">Á síðunni **Upplýsingar um afurð**:</span><span class="sxs-lookup"><span data-stu-id="672e9-110">On the **Product details** page:</span></span>

    - <span data-ttu-id="672e9-111">Ef aðili tengdur verslun fer á síðuna **Upplýsingar um afurð** þegar hann skoðar fyrri færslur þvert á mismunandi rásir stingur þjónustan upp á fleiri vörum sem eru líklegar til að vera keyptar saman.</span><span class="sxs-lookup"><span data-stu-id="672e9-111">If a store associate visits a **Product details** page when looking at previous transactions across different channels, the recommendations service suggests additional items that are likely to be purchased together.</span></span>

    <span data-ttu-id="672e9-112">[![Meðmæli á upplýsingasíðu afurðar](./media/proddetails.png)](./media/proddetails.png)</span><span class="sxs-lookup"><span data-stu-id="672e9-112">[![Recommendations on the Product details page](./media/proddetails.png)](./media/proddetails.png)</span></span>

2. <span data-ttu-id="672e9-113">Á síðunni **Færsla**:</span><span class="sxs-lookup"><span data-stu-id="672e9-113">On the **Transaction** page:</span></span>

    - <span data-ttu-id="672e9-114">Ráðgjafarvélin leggur til hluti sem byggja á öllum listanum yfir hluti í körfunni sem oft eru keyptir saman.</span><span class="sxs-lookup"><span data-stu-id="672e9-114">The recommendation engine suggests items based on the entire list of items in the basket that are frequently bought together.</span></span>

    > [!NOTE]
    > <span data-ttu-id="672e9-115">Til að birta ráðleggingar á síðunni **Færsla** þarf smásöluaðilinn að uppfæra skjáútlitið í Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="672e9-115">To display recommendations on the **Transaction** page, the retailer needs to update the screen layout in Dynamics 365 Commerce.</span></span> <span data-ttu-id="672e9-116">Sleppa verður stýringunni **Ráðleggingar** á síðuna **Færsla**.</span><span class="sxs-lookup"><span data-stu-id="672e9-116">The **Recommendations** control must be dropped onto the **Transaction** page.</span></span>

    <span data-ttu-id="672e9-117">[![Meðmæli á færslusíðunni](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)</span><span class="sxs-lookup"><span data-stu-id="672e9-117">[![Recommendations on the Transaction page](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)</span></span>

## <a name="configure-commerce-to-enable-pos-recommendations"></a><span data-ttu-id="672e9-118">Skilgreina Commerce til að virkja ráðleggingar sölustaðar</span><span class="sxs-lookup"><span data-stu-id="672e9-118">Configure Commerce to enable POS recommendations</span></span>

<span data-ttu-id="672e9-119">Til að setja upp vöruráðleggingar skal fylgja þessum skrefum:</span><span class="sxs-lookup"><span data-stu-id="672e9-119">To set up product recommendations, follow these steps:</span></span>

1. <span data-ttu-id="672e9-120">Gakktu úr skugga um að þjónusta þín hafi verið uppfærð í **10.0.6 bygging.**</span><span class="sxs-lookup"><span data-stu-id="672e9-120">Ensure your service has been updated to the **10.0.6 build.**</span></span>
2. <span data-ttu-id="672e9-121">Fylgdu leiðbeiningunum um hvernig á að gera [virkja tillögur um vöru](../commerce/enable-product-recommendations.md) fyrir fyrirtæki þitt.</span><span class="sxs-lookup"><span data-stu-id="672e9-121">Follow the instructions on how to [enable product recommendations](../commerce/enable-product-recommendations.md) for your business.</span></span>
3. <span data-ttu-id="672e9-122">Valfrjálst: Til Að birta ráðleggingar á færsluskjánum, er farið í **Útlit Skjás**útlit skjás valið **Útlitshönnuður afgreiðsluskjás** opnaður, og svo sleppt stýringunni **leiðbeiningar** þar sem þarf.</span><span class="sxs-lookup"><span data-stu-id="672e9-122">Optional: To display recommendations on the transaction screen, go to **Screen Layout**, choose your screen layout, launch the **Screen layout designer**, and then drop the **recommendations** control where needed.</span></span>
4. <span data-ttu-id="672e9-123">Farið í **Færibreytur Commerce**, veljið **Vélnám** svo **Já** undir **virkja ráðleggingar sölustaðar**.</span><span class="sxs-lookup"><span data-stu-id="672e9-123">Go to **Commerce parameters**, select **Machine-learning**, select **Yes** under **Enable POS recommendations**.</span></span>
5. <span data-ttu-id="672e9-124">Til að sjá ráðleggingar á sölustað skal keyra altæku vinnsluna **1110**.</span><span class="sxs-lookup"><span data-stu-id="672e9-124">To see recommendations on POS, run global configuration job **1110**.</span></span> <span data-ttu-id="672e9-125">Til að endurspegla breytingar á útlitshönnuði sölustaðar skal keyra skilgreiningarvinnslu rásar **1070**.</span><span class="sxs-lookup"><span data-stu-id="672e9-125">To reflect changes made to POS screen layout designer, run channel configuration job **1070**.</span></span>

## <a name="troubleshoot-issues-where-you-have-product-recommendations-already-enabled"></a><span data-ttu-id="672e9-126">Finna úrræði á vandamálum þar sem ráðleggingar um vörur hafa þegar verið virkjaðar</span><span class="sxs-lookup"><span data-stu-id="672e9-126">Troubleshoot issues where you have Product recommendations already enabled</span></span>

- <span data-ttu-id="672e9-127">Flettið upp á **Færibreytur Commerce** \> **Ráðleggingalistar** \> **Slökkva á ráðleggingum um vörur** og keyrið **Altæka skilgreiningarvinnslu \[9999\]**.</span><span class="sxs-lookup"><span data-stu-id="672e9-127">Navigate to **Commerce Parameters** \> **Recommendation lists** \> **Disable product recommendations** and run **Global configuration job \[9999\]**.</span></span> 
- <span data-ttu-id="672e9-128">Ef **Stýringu ráðleggingar** var bætt við færsluskjáinn með því að nota **Útlitshönnun afgreiðsluskjás** skaltu fjarlægja hana líka.</span><span class="sxs-lookup"><span data-stu-id="672e9-128">If you added the **Recommendations control** to your transaction screen using the **Screen layout designer**, please remove that as well.</span></span>
- <span data-ttu-id="672e9-129">Ef þú hefur frekari spurningar skaltu skoða [Algengar spurningar um afurðaráðleggingar](../commerce/faq-recommendations.md) fyrir meiri upplýsingar.</span><span class="sxs-lookup"><span data-stu-id="672e9-129">If you have additional questions, check out the [Product recommendations FAQ](../commerce/faq-recommendations.md) for more information.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="672e9-130">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="672e9-130">Additional resources</span></span>

[<span data-ttu-id="672e9-131">Bæta stýringu ráðleggingar á færsluskjá á sölustaðartækjum</span><span class="sxs-lookup"><span data-stu-id="672e9-131">Add a recommendations control to the transaction screen on POS devices</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="672e9-132">Yfirlit yfir afurðarráðleggingar</span><span class="sxs-lookup"><span data-stu-id="672e9-132">Product recommendations overview</span></span>](../commerce/product-recommendations.md)

[<span data-ttu-id="672e9-133">Virkja ráðleggingar um afurðir</span><span class="sxs-lookup"><span data-stu-id="672e9-133">Enable product recommendations</span></span>](../commerce/enable-product-recommendations.md) 
