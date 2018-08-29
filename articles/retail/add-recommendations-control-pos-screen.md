---
title: "Bæta stýringu ráðleggingar á færsluskjá á sölustaðartækjum"
description: "Þetta efnisatriði lýsir hvernig á að bæta ráðleggingarstjórnun við færsluskjáinn á sölustaðartæki (POS) og nota til þess útlitshönnun skjás í Microsoft Dynamics 365 for Retail."
author: ashishmsft
manager: AnnBe
ms.date: 02/05/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
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
ms.translationtype: HT
ms.sourcegitcommit: 5098fb3339403b6f2779dfe3bb7ef5c4ca78051f
ms.openlocfilehash: 26b03b6712c97b12e1221598de308813c7986179
ms.contentlocale: is-is
ms.lasthandoff: 08/09/2018

---

# <a name="add-a-recommendations-control-to-the-transaction-screen-on-pos-devices"></a><span data-ttu-id="a21df-103">Bæta stýringu ráðleggingar á færsluskjá á sölustaðartækjum</span><span class="sxs-lookup"><span data-stu-id="a21df-103">Add a recommendations control to the transaction screen on POS devices</span></span>

[!include [banner](includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="a21df-104">Núverandi útgáfa af ráðleggingaþjónustu vörunnar verður fjarlægð og eiginleikinn endurhannaður með betra reikniriti og nýrri smásölumiðuðum möguleikum.</span><span class="sxs-lookup"><span data-stu-id="a21df-104">We are removing the current version of the product recommendation service as we redesign this feature with a better algorithm and newer retail-oriented capabilities.</span></span> <span data-ttu-id="a21df-105">Sjá [Fjarlægðir eða úreltir eiginleikar](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/migration-upgrade/deprecated-features) fyrir frekari upplýsingar.</span><span class="sxs-lookup"><span data-stu-id="a21df-105">For more information see [Removed or deprecated features](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/migration-upgrade/deprecated-features).</span></span> 

<span data-ttu-id="a21df-106">Þetta efnisatriði lýsir hvernig á að bæta ráðleggingarstjórnun við færsluskjáinn á sölustaðartæki (POS) og nota til þess útlitshönnun skjás í Microsoft Dynamics 365 for Retail.</span><span class="sxs-lookup"><span data-stu-id="a21df-106">This topic describes how to add a recommendations control to the transaction screen on a point of sale (POS) device using the screen layout designer in Microsoft Dynamics 365 for Retail.</span></span>

<span data-ttu-id="a21df-107">Hægt er að birta afurðarráðleggingar í POS-tæki þegar Microsoft Dynamics 365 for Retail er notað.</span><span class="sxs-lookup"><span data-stu-id="a21df-107">You can display product recommendations on your POS device when you use Microsoft Dynamics 365 for Retail.</span></span> <span data-ttu-id="a21df-108">*Ráðleggingar* eru vörur sem viðskiptavinurinn kann að hafa áhuga á grundvelli sögu innkaupapantanir, vara á óskalista þeirra og vörur sem aðrir viðskiptavinir keyptu á netinu og í verslunum.</span><span class="sxs-lookup"><span data-stu-id="a21df-108">*Recommendations* are items that your customer might be interested in based on their purchase history, items in their wish list, and items that other customers purchased online and in brick-and-mortar stores.</span></span> <span data-ttu-id="a21df-109">Til að birta vöruráðleggingar þarf að bæta við stýringu á færsluskjáinn með útlitshönnuður afgreiðsluskjás.</span><span class="sxs-lookup"><span data-stu-id="a21df-109">To display product recommendations, you need to add a control to the transaction screen using the screen layout designer.</span></span>

## <a name="open-layout-designer"></a><span data-ttu-id="a21df-110">Opnaðu Útlitshönnuður afgreiðsluskjás</span><span class="sxs-lookup"><span data-stu-id="a21df-110">Open Layout designer</span></span>
1.  <span data-ttu-id="a21df-111">Farðu í **Smásala** &gt; **Uppsetning rásar** &gt; **Uppsetning POS** &gt; **POS** &gt; **Skjáútlit**.</span><span class="sxs-lookup"><span data-stu-id="a21df-111">Go to **Retail** &gt; **Channel setup** &gt; **POS setup** &gt; **POS** &gt; **Screen layouts**.</span></span>
2.  <span data-ttu-id="a21df-112">Notaðu flýtiafmörkun til að finna skjáinn sem á að bæta stýringunni við.</span><span class="sxs-lookup"><span data-stu-id="a21df-112">Use the Quick Filter to find the screen that you want to add the control to.</span></span> <span data-ttu-id="a21df-113">Til dæmis notar sían í svæðinu **Útlitskenni afgreiðsluskjás** gildið 'F2CP16:9M'.</span><span class="sxs-lookup"><span data-stu-id="a21df-113">For example, filter on the **Screen layout ID** field using a value of ‘F2CP16:9M’.</span></span>
3.  <span data-ttu-id="a21df-114">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="a21df-114">In the list, find and select the desired record.</span></span> <span data-ttu-id="a21df-115">Til dæmis veldu ‘Nafn: F2CP16:9M Útlitskenni afgreiðsluskjás: F2CP16:9M’.</span><span class="sxs-lookup"><span data-stu-id="a21df-115">For example, select ‘Name: F2CP16:9M Screen Layout ID: F2CP16:9M’.</span></span>
4.  <span data-ttu-id="a21df-116">Smellt er á **Útlitshönnuður**.</span><span class="sxs-lookup"><span data-stu-id="a21df-116">Click **Layout designer**.</span></span>
5.  <span data-ttu-id="a21df-117">Fylgdu kvaðningum til að hefja Útlitshönnuðinn.</span><span class="sxs-lookup"><span data-stu-id="a21df-117">Follow the prompts to launch the layout designer.</span></span> <span data-ttu-id="a21df-118">Þegar beðið er um skilríki skal slá inn sömu skilríki og voru notuð þegar Útlitshönnuður var opnaður af síðunni **Skjáútlit**.</span><span class="sxs-lookup"><span data-stu-id="a21df-118">When prompted for credentials, enter the same credentials that were in use when the Layout designer was launched from **Screen layouts** page.</span></span>
6.  <span data-ttu-id="a21df-119">Þegar þú skráir þig inn birtist síða sem er svipuð þeirra sem er fyrir neðan.</span><span class="sxs-lookup"><span data-stu-id="a21df-119">When you log in, a page similar to the one below appears.</span></span> <span data-ttu-id="a21df-120">Útlitið verður mismunandi eftir þeim sérstillingum sem voru gerðar fyrir verslunina.</span><span class="sxs-lookup"><span data-stu-id="a21df-120">The layout will be different depending on the customizations that were made for your store.</span></span>

<span data-ttu-id="a21df-121">[![screenlayout-pic-1](./media/screenlayout-pic-1.png)](./media/screenlayout-pic-1.png) Veljið birta valkostur</span><span class="sxs-lookup"><span data-stu-id="a21df-121">[![screenlayout-pic-1](./media/screenlayout-pic-1.png)](./media/screenlayout-pic-1.png) Choose a display option</span></span>
-----------------------

<span data-ttu-id="a21df-122">Tvær skilgreiningar eru í boði:</span><span class="sxs-lookup"><span data-stu-id="a21df-122">There are two configurations options available.</span></span> <span data-ttu-id="a21df-123">Veldu valkostinn sem virkar best fyrir verslunina og fylgdu eftirstöðvum leiðbeininga til að ljúka uppsetningu stýringarinnar.</span><span class="sxs-lookup"><span data-stu-id="a21df-123">Choose the option that works best for your store, and follow the remaining instructions to finish setting up the control.</span></span> <span data-ttu-id="a21df-124">Valkostirnir tveir eru:</span><span class="sxs-lookup"><span data-stu-id="a21df-124">The two options are:</span></span>
-   <span data-ttu-id="a21df-125">Ráðleggingar eru alltaf sýnilegar.</span><span class="sxs-lookup"><span data-stu-id="a21df-125">Recommendations are always visible.</span></span>
-   <span data-ttu-id="a21df-126">Flipinn **Ráðleggingar** birtist í hnitanetinu hægra megin á skjánum.</span><span class="sxs-lookup"><span data-stu-id="a21df-126">A **Recommendations** tab appears in the grid on the right side of the screen.</span></span>

#### <a name="to-make-recommendations-always-visible"></a><span data-ttu-id="a21df-127">Til að gera ráðleggingar alltaf sýnilegar</span><span class="sxs-lookup"><span data-stu-id="a21df-127">To make recommendations always visible</span></span>

1.  <span data-ttu-id="a21df-128">Dragðu úr hæð upplýsingasvæðis færslulína svo að það sé í sömu hæð og svæði viðskiptamanns til vinstri.[](./media/pic-2.png)[![screenlayout-pic-2](./media/screenlayout-pic-2.png)](./media/screenlayout-pic-2.png)</span><span class="sxs-lookup"><span data-stu-id="a21df-128">Reduce the height of the transaction lines details area so that it is the same height as the customer panel to its left.[](./media/pic-2.png)[![screenlayout-pic-2](./media/screenlayout-pic-2.png)](./media/screenlayout-pic-2.png)</span></span>
2.  <span data-ttu-id="a21df-129">Frá valmynd til vinstri skal draga og sleppa ráðleggingarstýringu á milli upplýsingasvæðis færslulína og hnappahnita í neðst á miðjan færsluskjáinn.</span><span class="sxs-lookup"><span data-stu-id="a21df-129">From the menu on the left, drag and drop the recommendations control to between the transaction line details area and the button grid in the center bottom of the transaction screen.</span></span> <span data-ttu-id="a21df-130">Breyta stærð stýringar svo að hún passi í það bil.[](./media/pic-3.png)[![screenlayout-pic-3](./media/screenlayout-pic-3.png)](./media/screenlayout-pic-3.png)</span><span class="sxs-lookup"><span data-stu-id="a21df-130">Resize the control so it fits in that space.[](./media/pic-3.png)[![screenlayout-pic-3](./media/screenlayout-pic-3.png)](./media/screenlayout-pic-3.png)</span></span>
3.  <span data-ttu-id="a21df-131">Smellt er á **X++** til að vista og fara úr Útlitshönnuði.</span><span class="sxs-lookup"><span data-stu-id="a21df-131">Click the **X** to save and exit Layout designer.</span></span>
4.  <span data-ttu-id="a21df-132">Í Dynamics 365 for Retail er farið í **Smásala** &gt; **Upplýsingatækni smásölu** &gt; **Dreifingaráætlanir**.</span><span class="sxs-lookup"><span data-stu-id="a21df-132">In Dynamics 365 for Retail, go to **Retail** &gt; **Retail IT** &gt; **Distribution schedules**.</span></span>
5.  <span data-ttu-id="a21df-133">Á listanum velurðu **1090 afgreiðslukassar**.</span><span class="sxs-lookup"><span data-stu-id="a21df-133">In the list, select **1090 Registers**.</span></span>
6.  <span data-ttu-id="a21df-134">Smellt er á **Keyra núna**.</span><span class="sxs-lookup"><span data-stu-id="a21df-134">Click **Run now**.</span></span>

#### <a name="to-add-a-recommendations-tab-to-the-button-grid-on-the-right-side-of-the-screen"></a><span data-ttu-id="a21df-135">Til að bæta við ráðleggingaflipa í hnitanetið hægra megin á skjánum</span><span class="sxs-lookup"><span data-stu-id="a21df-135">To add a Recommendations tab to the button grid on the right side of the screen</span></span>

1.  <span data-ttu-id="a21df-136">Hægrismelltu í tómt bil undir síðasta flipanum á hnappahnitinu hægra megin á síðunni.</span><span class="sxs-lookup"><span data-stu-id="a21df-136">Right-click in the empty space below the last tab on the button grid located on the right side of the page.</span></span>
2.  <span data-ttu-id="a21df-137">Smellt er á **Sérstilla**.[![pic-5](./media/pic-5.png)](./media/pic-5.png)</span><span class="sxs-lookup"><span data-stu-id="a21df-137">Click **Customize**.[![pic-5](./media/pic-5.png)](./media/pic-5.png)</span></span>
3.  <span data-ttu-id="a21df-138">Smellt er á **Nýr flipi**.</span><span class="sxs-lookup"><span data-stu-id="a21df-138">Click **New tab**.</span></span>
4.  <span data-ttu-id="a21df-139">Finndu nýja flipann sem þú varst að bæta við.</span><span class="sxs-lookup"><span data-stu-id="a21df-139">Find the new tab that you just added.</span></span> <span data-ttu-id="a21df-140">Þörf getur verið á því að skruna niður.</span><span class="sxs-lookup"><span data-stu-id="a21df-140">You may need to scroll down.</span></span>
5.  <span data-ttu-id="a21df-141">Í fellilistanum **Efni** skal velja **Ráðlögð afurð**.</span><span class="sxs-lookup"><span data-stu-id="a21df-141">In the **Contents** drop-down, select **Recommended products**.</span></span> <span data-ttu-id="a21df-142">[![pic-6](./media/pic-6.png)](./media/pic-6.png)</span><span class="sxs-lookup"><span data-stu-id="a21df-142">[![pic-6](./media/pic-6.png)](./media/pic-6.png)</span></span>
6.  <span data-ttu-id="a21df-143">Á svæðinu **Merkimiði** skal færa inn heiti sniðsins. Til dæmis, ritarðu ‚Ráðlagðar vörur‘.</span><span class="sxs-lookup"><span data-stu-id="a21df-143">In the **Label** field, type a name for the recommendations tab. For example, type ‘Recommended products’.</span></span>
7.  <span data-ttu-id="a21df-144">Í svæðinu **Mynd** velurðu myndina sem á að birtast á flipanum.</span><span class="sxs-lookup"><span data-stu-id="a21df-144">In the **Image** field, select the image to appear on the tab.</span></span>
8.  <span data-ttu-id="a21df-145">Smellt er á **OK**.</span><span class="sxs-lookup"><span data-stu-id="a21df-145">Click **OK**.</span></span> <span data-ttu-id="a21df-146">Nýi flipinn birtist í hnappahnitunum.</span><span class="sxs-lookup"><span data-stu-id="a21df-146">The new tab appears in the button grid.</span></span>
9.  <span data-ttu-id="a21df-147">Smellt er á **X++** til að vista og fara úr Útlitshönnuði.</span><span class="sxs-lookup"><span data-stu-id="a21df-147">Click the **X** to save and exit Layout designer.</span></span>
10. <span data-ttu-id="a21df-148">Í Dynamics 365 for Retail er farið í **Smásala** &gt; **Upplýsingatækni smásölu** &gt; **Dreifingaráætlanir**.</span><span class="sxs-lookup"><span data-stu-id="a21df-148">In Dynamics 365 for Retail, go to **Retail** &gt; **Retail IT** &gt; **Distribution schedules**.</span></span>
11. <span data-ttu-id="a21df-149">Á listanum velurðu **1090 afgreiðslukassar**.</span><span class="sxs-lookup"><span data-stu-id="a21df-149">In the list, select **1090 Registers**.</span></span>
12. <span data-ttu-id="a21df-150">Smellt er á **Keyra núna**.</span><span class="sxs-lookup"><span data-stu-id="a21df-150">Click **Run now**.</span></span>


<a name="additional-resources"></a><span data-ttu-id="a21df-151">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="a21df-151">Additional resources</span></span>
--------

[<span data-ttu-id="a21df-152">Yfirlit yfir sérsniðnar afurðarráðleggingar</span><span class="sxs-lookup"><span data-stu-id="a21df-152">Personalized product recommendations overview</span></span>](personalized-product-recommendations.md)




