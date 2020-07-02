---
title: Bæta við tillögum á færsluskjáinn
description: Þetta efnisatriði lýsir hvernig á að bæta við ráðleggingastýringu við færsluskjáinn á sölustaðartæki (POS) sem notar útlitshönnun skjás í Microsoft Dynamics 365 Commerce.
author: bebeale
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
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
ms.openlocfilehash: 760e6e093dbe0ba6b2781f90af7fbb614c492b93
ms.sourcegitcommit: ac47e8679fb104515f7dcca509294264bd05d2b1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/15/2020
ms.locfileid: "3454580"
---
# <a name="add-recommendations-to-the-transaction-screen"></a><span data-ttu-id="56cd6-103">Bæta við tillögum á færsluskjáinn</span><span class="sxs-lookup"><span data-stu-id="56cd6-103">Add recommendations to the transaction screen</span></span>

[!include [banner](includes/banner.md)]


<span data-ttu-id="56cd6-104">Þetta efnisatriði lýsir hvernig á að bæta við ráðleggingastýringu við færsluskjáinn á sölustaðartæki (POS) sem notar útlitshönnun skjás í Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="56cd6-104">This topic describes how to add a recommendations control to the transaction screen on a point of sale (POS) device using the screen layout designer in Microsoft Dynamics 365 Commerce.</span></span> <span data-ttu-id="56cd6-105">Nánari upplýsingar um ráðleggingar um vöru er að finna í [ráðleggingar um vörur í POS-skjölum](product.md).</span><span class="sxs-lookup"><span data-stu-id="56cd6-105">For more information about product recommendations, read the  [product recommendations on POS documentation](product.md).</span></span>


<span data-ttu-id="56cd6-106">Hægt er að sýna vöruráðleggingar í POS-tækinu þegar þú notar Commerce.</span><span class="sxs-lookup"><span data-stu-id="56cd6-106">You can display product recommendations on your POS device when you use Commerce.</span></span> <span data-ttu-id="56cd6-107">Til að birta vöruráðleggingar þarf að bæta við stýringu á færsluskjáinn með útlitshönnuður afgreiðsluskjás.</span><span class="sxs-lookup"><span data-stu-id="56cd6-107">To display product recommendations, you need to add a control to the transaction screen using the screen layout designer.</span></span> 

## <a name="open-layout-designer"></a><span data-ttu-id="56cd6-108">Opnaðu Útlitshönnuður afgreiðsluskjás</span><span class="sxs-lookup"><span data-stu-id="56cd6-108">Open Layout designer</span></span>

1. <span data-ttu-id="56cd6-109">Farðu í **Retail og Commerce** &gt; **Uppsetningu rásar** &gt; **Uppsetning POS** &gt; **POS** &gt; **Skjáútlit**.</span><span class="sxs-lookup"><span data-stu-id="56cd6-109">Go to **Retail and Commerce** &gt; **Channel setup** &gt; **POS setup** &gt; **POS** &gt; **Screen layouts**.</span></span>
2. <span data-ttu-id="56cd6-110">Notaðu flýtiafmörkun til að finna skjáinn sem á að bæta stýringunni við.</span><span class="sxs-lookup"><span data-stu-id="56cd6-110">Use the Quick Filter to find the screen that you want to add the control to.</span></span> <span data-ttu-id="56cd6-111">Til dæmis notar sían í svæðinu **Útlitskenni afgreiðsluskjás** gildið **F2CP16:9M**.</span><span class="sxs-lookup"><span data-stu-id="56cd6-111">For example, filter on the **Screen layout ID** field using a value of **F2CP16:9M**.</span></span>
3. <span data-ttu-id="56cd6-112">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="56cd6-112">In the list, find and select the desired record.</span></span> <span data-ttu-id="56cd6-113">Til dæmis veldu **Nafn: F2CP16:9M Útlitskenni afgreiðsluskjás: F2CP16:9M**.</span><span class="sxs-lookup"><span data-stu-id="56cd6-113">For example, select **Name: F2CP16:9M Screen Layout ID: F2CP16:9M**.</span></span>
4. <span data-ttu-id="56cd6-114">Smellt er á **Útlitshönnuður**.</span><span class="sxs-lookup"><span data-stu-id="56cd6-114">Click **Layout designer**.</span></span>
5. <span data-ttu-id="56cd6-115">Fylgdu kvaðningum til að hefja Útlitshönnuðinn.</span><span class="sxs-lookup"><span data-stu-id="56cd6-115">Follow the prompts to launch the layout designer.</span></span> <span data-ttu-id="56cd6-116">Þegar beðið er um skilríki skal slá inn sömu skilríki og voru notuð þegar Útlitshönnuður var opnaður af síðunni **Skjáútlit**.</span><span class="sxs-lookup"><span data-stu-id="56cd6-116">When prompted for credentials, enter the same credentials that were in use when the Layout designer was launched from **Screen layouts** page.</span></span>
6. <span data-ttu-id="56cd6-117">Þegar þú skráir þig inn birtist síða sem er svipuð þeirra sem er fyrir neðan.</span><span class="sxs-lookup"><span data-stu-id="56cd6-117">When you log in, a page similar to the one below appears.</span></span> <span data-ttu-id="56cd6-118">Útlitið verður mismunandi eftir þeim sérstillingum sem voru gerðar fyrir verslunina.</span><span class="sxs-lookup"><span data-stu-id="56cd6-118">The layout will be different depending on the customizations that were made for your store.</span></span>


    <span data-ttu-id="56cd6-119">[![Útlitshönnuður](./media/screenlayout-pic-1.png)](./media/screenlayout-pic-1.png)</span><span class="sxs-lookup"><span data-stu-id="56cd6-119">[![Layout designer](./media/screenlayout-pic-1.png)](./media/screenlayout-pic-1.png)</span></span>

## <a name="choose-a-display-option"></a><span data-ttu-id="56cd6-120">Veldu valkost skjás</span><span class="sxs-lookup"><span data-stu-id="56cd6-120">Choose a display option</span></span>

<span data-ttu-id="56cd6-121">Tvær skilgreiningar eru í boði:</span><span class="sxs-lookup"><span data-stu-id="56cd6-121">There are two configurations options available.</span></span> <span data-ttu-id="56cd6-122">Veldu valkostinn sem virkar best fyrir verslunina og fylgdu eftirstöðvum leiðbeininga til að ljúka uppsetningu stýringarinnar.</span><span class="sxs-lookup"><span data-stu-id="56cd6-122">Choose the option that works best for your store, and follow the remaining instructions to finish setting up the control.</span></span> <span data-ttu-id="56cd6-123">Valkostirnir tveir eru:</span><span class="sxs-lookup"><span data-stu-id="56cd6-123">The two options are:</span></span>

- <span data-ttu-id="56cd6-124">Ráðleggingar eru alltaf sýnilegar.</span><span class="sxs-lookup"><span data-stu-id="56cd6-124">Recommendations are always visible.</span></span>
- <span data-ttu-id="56cd6-125">Flipinn **Ráðleggingar** birtist í hnitanetinu hægra megin á skjánum.</span><span class="sxs-lookup"><span data-stu-id="56cd6-125">A **Recommendations** tab appears in the grid on the right side of the screen.</span></span>

### <a name="make-recommendations-always-visible"></a><span data-ttu-id="56cd6-126">Gera ráðleggingar alltaf sýnilegar</span><span class="sxs-lookup"><span data-stu-id="56cd6-126">Make recommendations always visible</span></span>


1. <span data-ttu-id="56cd6-127">Dragðu úr hæð upplýsingasvæðis færslulína svo að það sé í sömu hæð og svæði viðskiptamanns til vinstri .</span><span class="sxs-lookup"><span data-stu-id="56cd6-127">Reduce the height of the transaction lines details area so that it is the same height as the customer panel to its left.</span></span>


    <span data-ttu-id="56cd6-128">[![Hæð á upplýsingasvæði fyrir færslulínur minnkuð](./media/screenlayout-pic-2.png)](./media/screenlayout-pic-2.png)</span><span class="sxs-lookup"><span data-stu-id="56cd6-128">[![Height of the transaction lines details area reduced](./media/screenlayout-pic-2.png)](./media/screenlayout-pic-2.png)</span></span>

2. <span data-ttu-id="56cd6-129">Frá valmynd til vinstri skal draga og sleppa ráðleggingarstýringu á milli upplýsingasvæðis færslulína og hnappahnita í neðst á miðjan færsluskjáinn.</span><span class="sxs-lookup"><span data-stu-id="56cd6-129">From the menu on the left, drag and drop the recommendations control to between the transaction line details area and the button grid in the center bottom of the transaction screen.</span></span> <span data-ttu-id="56cd6-130">Breyta stærð stýringar svo að hún passi í það bil.</span><span class="sxs-lookup"><span data-stu-id="56cd6-130">Resize the control so it fits in that space.</span></span>

    <span data-ttu-id="56cd6-131">[![Ráðleggingarstýringu bætt við útlitið](./media/screenlayout-pic-3.png)](./media/screenlayout-pic-3.png)</span><span class="sxs-lookup"><span data-stu-id="56cd6-131">[![Recommendations control added to the layout](./media/screenlayout-pic-3.png)](./media/screenlayout-pic-3.png)</span></span>


3. <span data-ttu-id="56cd6-132">Smellt er á **X++** til að vista og fara úr Útlitshönnuði.</span><span class="sxs-lookup"><span data-stu-id="56cd6-132">Click the **X** to save and exit Layout designer.</span></span>
4. <span data-ttu-id="56cd6-133">Í Commerce er farið í **Retail og Commerce** &gt; **upplýsingatækni í Retail og Commerce** &gt; **dreifingaráætlun**.</span><span class="sxs-lookup"><span data-stu-id="56cd6-133">In Commerce, go to **Retail and Commerce** &gt; **Retail and Commerce IT** &gt; **Distribution schedules**.</span></span>
5. <span data-ttu-id="56cd6-134">Á listanum velurðu **1090 afgreiðslukassar**.</span><span class="sxs-lookup"><span data-stu-id="56cd6-134">In the list, select **1090 Registers**.</span></span>
6. <span data-ttu-id="56cd6-135">Smellt er á **Keyra núna**.</span><span class="sxs-lookup"><span data-stu-id="56cd6-135">Click **Run now**.</span></span>


### <a name="add-a-recommendations-tab-to-the-button-grid-on-the-right-side-of-the-screen"></a><span data-ttu-id="56cd6-136">Bæta ráðleggingaflipa við hnitanetið hægra megin á skjánum</span><span class="sxs-lookup"><span data-stu-id="56cd6-136">Add a Recommendations tab to the button grid on the right side of the screen</span></span>

1. <span data-ttu-id="56cd6-137">Hægrismelltu í tómt bil undir síðasta flipanum á hnappahnitinu hægra megin á síðunni.</span><span class="sxs-lookup"><span data-stu-id="56cd6-137">Right-click in the empty space below the last tab on the button grid located on the right side of the page.</span></span>

2. <span data-ttu-id="56cd6-138">Smelltu á **Sérstilla**.</span><span class="sxs-lookup"><span data-stu-id="56cd6-138">Click **Customize**.</span></span>

    <span data-ttu-id="56cd6-139">[![Sérstilling - Svargluggi flipastýringar](./media/pic-5.png)](./media/pic-5.png)</span><span class="sxs-lookup"><span data-stu-id="56cd6-139">[![Customization - Tab control dialog box](./media/pic-5.png)](./media/pic-5.png)</span></span>

3. <span data-ttu-id="56cd6-140">Smellt er á **Nýr flipi**.</span><span class="sxs-lookup"><span data-stu-id="56cd6-140">Click **New tab**.</span></span>
4. <span data-ttu-id="56cd6-141">Finndu nýja flipann sem þú varst að bæta við.</span><span class="sxs-lookup"><span data-stu-id="56cd6-141">Find the new tab that you just added.</span></span> <span data-ttu-id="56cd6-142">Hugsanlega þarf að skruna niður.</span><span class="sxs-lookup"><span data-stu-id="56cd6-142">You may need to scroll down.</span></span>
5. <span data-ttu-id="56cd6-143">Í fellilistanum **Efni** skal velja **Ráðlögð afurð**.</span><span class="sxs-lookup"><span data-stu-id="56cd6-143">In the **Contents** drop-down, select **Recommended products**.</span></span>

    <span data-ttu-id="56cd6-144">[![Val á vörum sem mælt er með í efnisreitnum](./media/pic-6.png)](./media/pic-6.png)</span><span class="sxs-lookup"><span data-stu-id="56cd6-144">[![Selecting Recommended products in the Contents field](./media/pic-6.png)](./media/pic-6.png)</span></span>

6. <span data-ttu-id="56cd6-145">Í svæðinu **Merki** skal færa inn heiti á ráðleggingaflipanum. Færðu til dæmis inn „Ráðlagðar afurðir“.</span><span class="sxs-lookup"><span data-stu-id="56cd6-145">In the **Label** field, type a name for the recommendations tab. For example, type 'Recommended products'.</span></span>
7. <span data-ttu-id="56cd6-146">Í svæðinu **Mynd** velurðu myndina sem á að birtast á flipanum.</span><span class="sxs-lookup"><span data-stu-id="56cd6-146">In the **Image** field, select the image to appear on the tab.</span></span>
8. <span data-ttu-id="56cd6-147">Smellt er á **OK**.</span><span class="sxs-lookup"><span data-stu-id="56cd6-147">Click **OK**.</span></span> <span data-ttu-id="56cd6-148">Nýi flipinn birtist í hnappahnitunum.</span><span class="sxs-lookup"><span data-stu-id="56cd6-148">The new tab appears in the button grid.</span></span>
9. <span data-ttu-id="56cd6-149">Smellt er á **X++** til að vista og fara úr Útlitshönnuði.</span><span class="sxs-lookup"><span data-stu-id="56cd6-149">Click the **X** to save and exit Layout designer.</span></span>
10. <span data-ttu-id="56cd6-150">Í Commerce er farið í **Retail og Commerce** &gt; **upplýsingatækni í Retail og Commerce** &gt; **dreifingaráætlun**.</span><span class="sxs-lookup"><span data-stu-id="56cd6-150">In Commerce, go to **Retail and Commerce** &gt; **Retail and Commerce IT** &gt; **Distribution schedules**.</span></span>
11. <span data-ttu-id="56cd6-151">Á listanum velurðu **1090 afgreiðslukassar**.</span><span class="sxs-lookup"><span data-stu-id="56cd6-151">In the list, select **1090 Registers**.</span></span>
12. <span data-ttu-id="56cd6-152">Smellt er á **Keyra núna**.</span><span class="sxs-lookup"><span data-stu-id="56cd6-152">Click **Run now**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="56cd6-153">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="56cd6-153">Additional resources</span></span>

[<span data-ttu-id="56cd6-154">Yfirlit yfir afurðarráðleggingar</span><span class="sxs-lookup"><span data-stu-id="56cd6-154">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="56cd6-155">Virkja Azure Data Lake Storage í Dynamics 365 Commerce-umhverfi</span><span class="sxs-lookup"><span data-stu-id="56cd6-155">Enable Azure Data Lake Storage in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="56cd6-156">Virkja ráðleggingar um afurðir</span><span class="sxs-lookup"><span data-stu-id="56cd6-156">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="56cd6-157">Kveikja á sérsniðnum tillögum</span><span class="sxs-lookup"><span data-stu-id="56cd6-157">Enable personalized recommendations</span></span>](personalized-recommendations.md)

[<span data-ttu-id="56cd6-158">Afþakka sérsniðnar tillögur</span><span class="sxs-lookup"><span data-stu-id="56cd6-158">Opt out of personalized recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="56cd6-159">Bæta við afurðatillögum á sölustað</span><span class="sxs-lookup"><span data-stu-id="56cd6-159">Add product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="56cd6-160">Aðlagaðu niðurstöður AI-ML</span><span class="sxs-lookup"><span data-stu-id="56cd6-160">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="56cd6-161">Búðu til handvirkt myndaðar ráðleggingar</span><span class="sxs-lookup"><span data-stu-id="56cd6-161">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="56cd6-162">Búðu til tillögur með kynningargögnum</span><span class="sxs-lookup"><span data-stu-id="56cd6-162">Create recommendations with demo data</span></span>](product-recommendations-demo-data.md)

[<span data-ttu-id="56cd6-163">Algengar spurningar um afurðaráðleggingar</span><span class="sxs-lookup"><span data-stu-id="56cd6-163">Product recommendations FAQ</span></span>](faq-recommendations.md)
