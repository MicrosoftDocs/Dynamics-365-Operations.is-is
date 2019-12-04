---
title: Leysisstefna fyrir afurðarafbrigði
description: Þetta efnisatriði lýsir því hvernig hægt er að nota leysisstefnu til að bæta árangur afurðarafbrigðis.
author: cvocph
manager: AnnBe
ms.date: 02/19/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PCCreateProductConfigurationModel, PCProductConfigurationModelListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 241e1ae9bfd347695d7a2dbb7b3e71a7d49c2b93
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/18/2019
ms.locfileid: "2814537"
---
# <a name="solver-strategy-for-product-configuration"></a><span data-ttu-id="8a305-103">Leysisstefna fyrir afurðarafbrigði</span><span class="sxs-lookup"><span data-stu-id="8a305-103">Solver strategy for product configuration</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8a305-104">Þetta efnisatriði lýsir því hvernig hægt er að nota leysisstefnu til að bæta árangur afurðarafbrigðis.</span><span class="sxs-lookup"><span data-stu-id="8a305-104">This topic describes how you can use the solver strategy to improve the performance of product configuration.</span></span>

<span data-ttu-id="8a305-105">Hugmyndin um leysisstefnu var fyrst kynnt í heildaruppfærslu 7 (CU7) for Microsoft Dynamics AX 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="8a305-105">The concept of solver strategies was first introduced in Cumulative update 7 (CU7) for Microsoft Dynamics AX 2012 R2.</span></span> <span data-ttu-id="8a305-106">Hún var útvíkkuð í heildaruppfærslu 8 (CU8) fyrir Microsoft Dynamics AX 2012 R3 og Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition 7.3.</span><span class="sxs-lookup"><span data-stu-id="8a305-106">It was extended in Cumulative update 8 (CU8) for Microsoft Dynamics AX 2012 R3 and Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3.</span></span>

<span data-ttu-id="8a305-107">Hugmyndin um leysisstefnuna samanstendur nú af eftirfarandium lausnarmenn samanstendur nú af eftirfarandi aðferðum:</span><span class="sxs-lookup"><span data-stu-id="8a305-107">The solver strategy concept now consists of the following strategies:</span></span>

- <span data-ttu-id="8a305-108">Sjálfgefið</span><span class="sxs-lookup"><span data-stu-id="8a305-108">Default</span></span>
- <span data-ttu-id="8a305-109">Lágmarkslén fyrst</span><span class="sxs-lookup"><span data-stu-id="8a305-109">Minimal domains first</span></span>
- <span data-ttu-id="8a305-110">Ofan og niður</span><span class="sxs-lookup"><span data-stu-id="8a305-110">Top-down</span></span>
- <span data-ttu-id="8a305-111">Z3</span><span class="sxs-lookup"><span data-stu-id="8a305-111">Z3</span></span>

## <a name="solver-strategy"></a><span data-ttu-id="8a305-112">Leysisstefna</span><span class="sxs-lookup"><span data-stu-id="8a305-112">Solver strategy</span></span> 

<span data-ttu-id="8a305-113">Afrbrigðalíkan afurðar er hægt að móta sem [vandamál uppfylltra skilyrða (CSP)](http://aima.cs.berkeley.edu/2nd-ed/newchap05.pdf).</span><span class="sxs-lookup"><span data-stu-id="8a305-113">A product configuration model can be formulated as a [constraint satisfaction problem (CSP)](http://aima.cs.berkeley.edu/2nd-ed/newchap05.pdf).</span></span> <span data-ttu-id="8a305-114">Microsoft Solver Foundation (MSF) býður upp á tvær tegundir af leysisstefnum til að leysa CSP sem hægt er að nota úr afbrigðalíkönum afurðar.</span><span class="sxs-lookup"><span data-stu-id="8a305-114">Microsoft Solver Foundation (MSF) provides two types of solver strategies to solve the CSPs that can be used from product configuration models.</span></span> <span data-ttu-id="8a305-115">Þessar leysisstefnur reiða sig á [leiðsagnarreglur](https://techterms.com/definition/heuristic) sem eru notaðar til að ákvarða röðina sem breytur CSP eru taldar vera á meðan verið er að leysa úr vandamálinu.</span><span class="sxs-lookup"><span data-stu-id="8a305-115">These solver strategies rely on [heuristics](https://techterms.com/definition/heuristic), which are used to determine the order that the variables of the CSPs are considered in when the problem is being solved.</span></span> <span data-ttu-id="8a305-116">Leiðsagnarreglur geta haft veruleg áhrif á afköst á meðan verið er að leysa úr vandamálinu eða flokki vandamála.</span><span class="sxs-lookup"><span data-stu-id="8a305-116">Heuristics can significantly affect performance when a problem or class of problems is being solved.</span></span>

<span data-ttu-id="8a305-117">Leysisstefnan fyrir afbrigðalíkan afurðar ákvarðar hvaða sem skilgreinir hvaða lausn er notuð með leiðsagnarreglum.</span><span class="sxs-lookup"><span data-stu-id="8a305-117">The solver strategy for product configuration models determines which solver is used with heuristics.</span></span> <span data-ttu-id="8a305-118">Aðferðirnar **Sjálfgefið**, **Lágmarkslén fyrst** og **Ofan og niður** nota tvær lausnir fyrir MSF, á meðan **Z3** aðferðin notar Z3 lausn.</span><span class="sxs-lookup"><span data-stu-id="8a305-118">The **Default**, **Minimal domains first**, and **Top-down** strategies use the two solvers from MSF, whereas the **Z3** strategy uses the Z3 solver.</span></span> 

<span data-ttu-id="8a305-119">Framkvæmdarrannsóknir á raunverulegum viðskiptavini hafa sýnt að breyting á leysisstefnunni fyrir afbrigðalíkan afurðar getur dregið úr svartíma frá mínútum til millisekúndna.</span><span class="sxs-lookup"><span data-stu-id="8a305-119">Real customer implementation studies have shown that a change in the solver strategy for a product configuration model can reduce the response time from minutes to milliseconds.</span></span> <span data-ttu-id="8a305-120">Þess vegna er það þess virði að reyna að mismunandi leysisstefnur til að finna skilvirkustu stefnuna fyrir afbrigðalíkan afurðar.</span><span class="sxs-lookup"><span data-stu-id="8a305-120">Therefore, it's worth the effort to try different solver strategies to find the most efficient strategy for your product configuration model.</span></span>

## <a name="change-the-settings-for-the-solver-strategy"></a><span data-ttu-id="8a305-121">Breyta stillingum fyrir leysisstefnuna</span><span class="sxs-lookup"><span data-stu-id="8a305-121">Change the settings for the solver strategy</span></span>

<span data-ttu-id="8a305-122">Til að breyta leysisstefnunni, á síðunni **Afbrigðalíkan afurðar**, í aðgerðarglugganum, velurðu **Eiginleikar líkana**.</span><span class="sxs-lookup"><span data-stu-id="8a305-122">To change the solver strategy, on the **Product configuration models** page, on the Action Pane, select **Model properties**.</span></span> <span data-ttu-id="8a305-123">Síðan skaltu velja leysisstefnuna í svarglugganum **Breyta upplýsingum líkans**.</span><span class="sxs-lookup"><span data-stu-id="8a305-123">Then, in the **Edit the model details** dialog box, select a solver strategy.</span></span>

<span data-ttu-id="8a305-124">[![Breyta leysisstefnunni](./media/solver-strategy.png)](./media/solver-strategy.png)</span><span class="sxs-lookup"><span data-stu-id="8a305-124">[![Changing the solver strategy](./media/solver-strategy.png)](./media/solver-strategy.png)</span></span>

<span data-ttu-id="8a305-125">Eins og er, er ekkert sem sjálfkrafa greinir hvaða leysisstefna muni vera skilvirkasta stefnan fyrir afbrigðalíkan afurða sem er háð skilyrðum.</span><span class="sxs-lookup"><span data-stu-id="8a305-125">Currently, there is no logic that automatically detects which solver strategy will be the most efficient strategy for constraint-based product configuration.</span></span> <span data-ttu-id="8a305-126">Þess vegna verður þú að prófa hverja leysisstefnu fyrir sig.</span><span class="sxs-lookup"><span data-stu-id="8a305-126">Therefore, you must try the solver strategies one by one.</span></span>

<span data-ttu-id="8a305-127">Í eftirfarandi töflu eru ráðleggingar um leysisstefnur til að nota við ýmsar aðstæður.</span><span class="sxs-lookup"><span data-stu-id="8a305-127">The following table provides recommendations about the solver strategy to use in various scenarios.</span></span>

| <span data-ttu-id="8a305-128">Leysisstefna</span><span class="sxs-lookup"><span data-stu-id="8a305-128">Solver strategy</span></span>      | <span data-ttu-id="8a305-129">Notaðu stefnuna við þessar aðstæður</span><span class="sxs-lookup"><span data-stu-id="8a305-129">Use the strategy in this scenario</span></span> |
|----------------------|-----------------------------------|
| <span data-ttu-id="8a305-130">Sjálfgefið</span><span class="sxs-lookup"><span data-stu-id="8a305-130">Default</span></span>              | <span data-ttu-id="8a305-131">**Sjálfgefna** stefnan hefur verið fínstillt til að leysa líkön sem treysta á töfluskorðanir.</span><span class="sxs-lookup"><span data-stu-id="8a305-131">The **Default** strategy has been optimized to solve models that rely on table constraints.</span></span> <span data-ttu-id="8a305-132">Framkvæmdarrannsóknir viðskiptavinar hafa sýnt að þessi stefna sé skilvirkasta stefnan í aðstæðum þar sem töfluskorður eru mikið notaðar.</span><span class="sxs-lookup"><span data-stu-id="8a305-132">Customer implementation studies have shown that this strategy is the most efficient strategy in scenarios where table constraints are used extensively.</span></span> |
| <span data-ttu-id="8a305-133">Lágmarkslén fyrst</span><span class="sxs-lookup"><span data-stu-id="8a305-133">Minimal domains first</span></span> | <span data-ttu-id="8a305-134">**Lágmarkslén fyrst** og **Ofan og niður** stefnurnar eru nátengdar.</span><span class="sxs-lookup"><span data-stu-id="8a305-134">The **Minimal domains first** and **Top-down** strategies are closely related.</span></span> <span data-ttu-id="8a305-135">Framkvæmdarrannsóknir viðskiptavina hafa sýnt að stefnan **Ofan og niður** er betri en stefnan **Lágmarkslén fyrst**.</span><span class="sxs-lookup"><span data-stu-id="8a305-135">Customer implementation studies have shown that the **Top-down** strategy, outperforms the **Minimal domains first** strategy.</span></span> <span data-ttu-id="8a305-136">Hins vegar er stefnan **Lágmarkslén fyrst** haldið í vörunni fyrir afturvirka samhæfni.</span><span class="sxs-lookup"><span data-stu-id="8a305-136">However, the **Minimal domains first** strategy is kept in the product for backward compatibility.</span></span> <span data-ttu-id="8a305-137">Báðar þessar leysisstefnur hafa sýnt fram á meiri skilvirkni við að leysa líkön sem innihalda nokkrar reikningssegðir þar sem engar töfluskorður eru notaðar.</span><span class="sxs-lookup"><span data-stu-id="8a305-137">Both these solver strategies have been shown to be more efficient at solving models that contain several arithmetic expressions where no table constraints are used.</span></span> <span data-ttu-id="8a305-138">Hins vegar er stefnan **Sjálfgefið** í sumum tilfellum betri en þessar tvær stefnur.</span><span class="sxs-lookup"><span data-stu-id="8a305-138">However, in some cases, the **Default** strategy outperforms these two strategies.</span></span> <span data-ttu-id="8a305-139">Mundu því að prófa hverja stefnu fyrir sig.</span><span class="sxs-lookup"><span data-stu-id="8a305-139">Therefore, remember to try each strategy.</span></span> |
| <span data-ttu-id="8a305-140">Ofansækið</span><span class="sxs-lookup"><span data-stu-id="8a305-140">Top-down</span></span>             | <span data-ttu-id="8a305-141">**Lágmarkslén fyrst** og **Ofan og niður** stefnurnar eru nátengdar.</span><span class="sxs-lookup"><span data-stu-id="8a305-141">The **Minimal domains first** and **Top-down** strategies are closely related.</span></span> <span data-ttu-id="8a305-142">Framkvæmdarrannsóknir viðskiptavina hafa sýnt að stefnan **Ofan og niður** er betri en stefnan **Lágmarkslén fyrst**.</span><span class="sxs-lookup"><span data-stu-id="8a305-142">Customer implementation studies have shown that the **Top-down** strategy, outperforms the **Minimal domains first** strategy.</span></span> <span data-ttu-id="8a305-143">Hins vegar er stefnan **Lágmarkslén fyrst** haldið í vörunni fyrir afturvirka samhæfni.</span><span class="sxs-lookup"><span data-stu-id="8a305-143">However, the **Minimal domains first** strategy is kept in the product for backward compatibility.</span></span> <span data-ttu-id="8a305-144">Báðar þessar leysisstefnur hafa sýnt fram á meiri skilvirkni við að leysa líkön sem innihalda nokkrar reikningssegðir þar sem engar töfluskorður eru notaðar.</span><span class="sxs-lookup"><span data-stu-id="8a305-144">Both these solver strategies have been shown to be more efficient at solving models that contain several arithmetic expressions where no table constraints are used.</span></span> <span data-ttu-id="8a305-145">Hins vegar er stefnan **Sjálfgefið** í sumum tilfellum betri en þessar tvær stefnur.</span><span class="sxs-lookup"><span data-stu-id="8a305-145">However, in some cases, the **Default** strategy outperforms these two strategies.</span></span> <span data-ttu-id="8a305-146">Mundu því að prófa hverja stefnu fyrir sig.</span><span class="sxs-lookup"><span data-stu-id="8a305-146">Therefore, remember to try each strategy.</span></span> |
| <span data-ttu-id="8a305-147">Z3</span><span class="sxs-lookup"><span data-stu-id="8a305-147">Z3</span></span>                   | <span data-ttu-id="8a305-148">Við mælum með því að þú notir stefenuna **Z3** sem sjálfgefna leysisstefnu.</span><span class="sxs-lookup"><span data-stu-id="8a305-148">We recommend that you use the **Z3** strategy as the default solver strategy.</span></span> <span data-ttu-id="8a305-149">Ef þú hefur áhyggjur af afköstum og sveigjanleika getur þú metið hinar stefnurnar.</span><span class="sxs-lookup"><span data-stu-id="8a305-149">If you're concerned about performance and scalability, you can evaluate the other strategies.</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="8a305-150">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="8a305-150">Additional resources</span></span>

[<span data-ttu-id="8a305-151">Yfirlit afurðarafbrigða</span><span class="sxs-lookup"><span data-stu-id="8a305-151">Product configuration overview</span></span>](build-product-configuration-model.md)

[<span data-ttu-id="8a305-152">Leiðsagnarreglur</span><span class="sxs-lookup"><span data-stu-id="8a305-152">Heuristics</span></span>](https://techterms.com/definition/heuristic)

[<span data-ttu-id="8a305-153">Vandamál uppfylltra skilyrði</span><span class="sxs-lookup"><span data-stu-id="8a305-153">Constraint Satisfaction Problem</span></span>](http://aima.cs.berkeley.edu/2nd-ed/newchap05.pdf)
