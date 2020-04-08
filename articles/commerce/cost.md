---
title: Skilgreining kostnaðar fyrir dreifingarstjórnun pöntunar (DOM)
description: Þetta efnisatriði lýsir skilgreiningu kostnaðar fyrir virkni dreifingarstjórnunar pöntunar (DOM) í Dynamics 365 Commerce.
author: josaw1
manager: AnnBe
ms.date: 12/05/2018
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-12-15
ms.dyn365.ops.version: ''
ms.openlocfilehash: 7644cb9800a418fd123b32a0257b787277fcb19f
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/01/2020
ms.locfileid: "3004229"
---
# <a name="cost-configuration-for-distributed-order-management-dom"></a><span data-ttu-id="ff2a7-103">Skilgreining kostnaðar fyrir dreifingarstjórnun pöntunar (DOM)</span><span class="sxs-lookup"><span data-stu-id="ff2a7-103">Cost configuration for distributed order management (DOM)</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ff2a7-104">Fyrirtæki íhuga marga kostnaðaríhluti til að ákvarða bestu staðsetninguna til að uppfylla pöntun frá.</span><span class="sxs-lookup"><span data-stu-id="ff2a7-104">Organizations consider multiple cost components to determine the optimal location to fulfill an order from.</span></span> <span data-ttu-id="ff2a7-105">Sumir þessara kostnaðaríhluta eru sendingarkostnaður, úrvinnslukostnaður og pökkunarkostnaður.</span><span class="sxs-lookup"><span data-stu-id="ff2a7-105">Some of these cost components are shipping cost, handling cost, and packaging cost.</span></span> <span data-ttu-id="ff2a7-106">Samsetning þessa kostnaðar er reiknaður til að ákvarða uppfyllingarstaðsetningu.</span><span class="sxs-lookup"><span data-stu-id="ff2a7-106">A combination of these costs is calculated to determine the fulfillment location.</span></span>

<span data-ttu-id="ff2a7-107">Þegar fyrsta ítrekun úthlutaðrar pantanastjórnunar (DOM) í Dynamics 365 Commerce fínstillti úthlutun pantana á uppfyllingarstaðsetningar var eingöngu vegalengd tekin með í reikninginn.</span><span class="sxs-lookup"><span data-stu-id="ff2a7-107">When the first iteration of distributed order management (DOM) in Dynamics 365 Commerce optimized the assignment of orders to fulfillment locations, it factored in distance only.</span></span> <span data-ttu-id="ff2a7-108">Vegalengd er ekki það sama og kostnaður þótt hægt sé að gera ráð fyrir henni í kostnaði.</span><span class="sxs-lookup"><span data-stu-id="ff2a7-108">Although distance can be correlated with cost, it isn't the same as cost.</span></span> <span data-ttu-id="ff2a7-109">Til dæmis kostar sendingarmáti að næturlagi meira en þriggja daga sending eða sjö daga sending sem felur í sér sömu vegalengdina.</span><span class="sxs-lookup"><span data-stu-id="ff2a7-109">For example, an overnight shipping method costs more than three-day shipping or seven-day shipping over the same distance.</span></span>

<span data-ttu-id="ff2a7-110">Eiginleiki kostnaðarskilgreiningar gerir söluaðilum kleift að skilgreina og grunnstilla aukalega kostnaðaríhluti sem verða reiknaðir og hafðir með til að ákvarða bestu staðsetninguna til að uppfylla pöntunarlínur frá.</span><span class="sxs-lookup"><span data-stu-id="ff2a7-110">The cost configuration feature lets retailers define and configure additional cost components that will be calculated and factored in to determine the optimal location to fulfill order lines from.</span></span>

<span data-ttu-id="ff2a7-111">Þegar kostnaðaríhlutir eru skilgreindir notar DOM-leysarinn eingöngu þessar kostnaðarskilgreiningar til að ákvarða bestu staðsetninguna til að uppfylla pöntun.</span><span class="sxs-lookup"><span data-stu-id="ff2a7-111">When cost components are configured, the DOM solver uses only those cost definitions to determine the optimal location for order fulfillment.</span></span> <span data-ttu-id="ff2a7-112">Hann tekur ekki vegalengd inn sem kostnað.</span><span class="sxs-lookup"><span data-stu-id="ff2a7-112">It doesn't consider the distance component as a cost.</span></span> <span data-ttu-id="ff2a7-113">Ef hins vegar engir kostnaðaríhlutir eru skilgreindir notar DOM-leysarinn vegalengd sem kostnað til að ákvarða bestu staðsetninguna til að uppfylla pöntun.</span><span class="sxs-lookup"><span data-stu-id="ff2a7-113">However, if no cost components are configured, the DOM solver does use the distance component as a cost to determine the optimal location for order fulfillment.</span></span>

## <a name="set-up-cost-components"></a><span data-ttu-id="ff2a7-114">Uppsetning kostnaðaríhluta</span><span class="sxs-lookup"><span data-stu-id="ff2a7-114">Set up cost components</span></span>

<span data-ttu-id="ff2a7-115">Hægt er að skilgreina tvær megingerðir kostnaðaríhluta í kerfinu: **Sending** og **Annað**.</span><span class="sxs-lookup"><span data-stu-id="ff2a7-115">Two major cost component types can be defined in the system: **Shipping** and **Other**.</span></span>

<span data-ttu-id="ff2a7-116">Báðar gerðir kostnaðaríhluta styðja marga útreikningsgrunna eins og sýnt er í eftirfarandi töflu.</span><span class="sxs-lookup"><span data-stu-id="ff2a7-116">Both cost component types support multiple calculation bases, as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="ff2a7-117">Gerð kostnaðaríhlutar</span><span class="sxs-lookup"><span data-stu-id="ff2a7-117">Cost component type</span></span></th>
<th><span data-ttu-id="ff2a7-118">Grunnur útreikninga</span><span class="sxs-lookup"><span data-stu-id="ff2a7-118">Calculation basis</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ff2a7-119">Sending</span><span class="sxs-lookup"><span data-stu-id="ff2a7-119">Shipping</span></span></td>
<td>
<ul>
<li><span data-ttu-id="ff2a7-120">Einfalt</span><span class="sxs-lookup"><span data-stu-id="ff2a7-120">Simple</span></span></li>
<li><span data-ttu-id="ff2a7-121">Lagskipt</span><span class="sxs-lookup"><span data-stu-id="ff2a7-121">Tiered</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="ff2a7-122">Annað</span><span class="sxs-lookup"><span data-stu-id="ff2a7-122">Other</span></span></td>
<td>
<ul>
<li><span data-ttu-id="ff2a7-123">Sölupöntun</span><span class="sxs-lookup"><span data-stu-id="ff2a7-123">Sales order</span></span></li>
<li><span data-ttu-id="ff2a7-124">Sölulínur</span><span class="sxs-lookup"><span data-stu-id="ff2a7-124">Sales line</span></span></li>
<li><span data-ttu-id="ff2a7-125">Staðsetning</span><span class="sxs-lookup"><span data-stu-id="ff2a7-125">Location</span></span></li>
</ul>
</td>
</tr>
</tbody>
</table>

### <a name="shipping-cost-component-type"></a><span data-ttu-id="ff2a7-126">Gerð íhlutar fyrir sendingarkostnað</span><span class="sxs-lookup"><span data-stu-id="ff2a7-126">Shipping cost component type</span></span>

<span data-ttu-id="ff2a7-127">Þessi hluti útskýrir hvernig á að setja upp hverja samsetningu fyrir sig fyrir kostnaðaríhlut af gerðinni **Sending** og útreikningsgrunn fyrir sendingarkostnað.</span><span class="sxs-lookup"><span data-stu-id="ff2a7-127">This section explains how to set up each combination of the **Shipping** cost component type and a calculation basis for shipping costs.</span></span> <span data-ttu-id="ff2a7-128">Þar er einnig útskýrt hvernig DOM-leysarinn notar hverja samsetningu.</span><span class="sxs-lookup"><span data-stu-id="ff2a7-128">It also explains how the DOM solver uses each combination.</span></span>

#### <a name="cost-component-type--shipping-and-calculation-basis--simple"></a><span data-ttu-id="ff2a7-129">Gerð kostnaðaríhlutar = sending og útreikningsgrunnur = einfaldur</span><span class="sxs-lookup"><span data-stu-id="ff2a7-129">Cost component type = Shipping and Calculation basis = Simple</span></span>

<span data-ttu-id="ff2a7-130">Ef samsetning kostnaðaríhlutar af gerðinni **Sending** og útreikningsgrunnurinn **Einfaldur** er notuð byggist sendingarkostnaður fyrir afhendingarmáta annaðhvort á flötum kostnaði eða vegalengd.</span><span class="sxs-lookup"><span data-stu-id="ff2a7-130">If a combination of the **Shipping** cost component type and the **Simple** calculation basis is used, the shipping cost for a mode of delivery is based on either a flat cost or distance.</span></span>

<span data-ttu-id="ff2a7-131">Setja verður upp eftirfarandi reiti fyrir þessa samsetningu:</span><span class="sxs-lookup"><span data-stu-id="ff2a7-131">You must set up the following fields for this combination:</span></span>

- <span data-ttu-id="ff2a7-132">**Kostnaðarstuðull** – Færið inn einkvæmt kennimerki fyrir kostnaðarstuðul.</span><span class="sxs-lookup"><span data-stu-id="ff2a7-132">**Cost factor** – Enter a unique identifier for the cost factor.</span></span>
- <span data-ttu-id="ff2a7-133">**Lýsing** – Færið inn heiti og lýsingu á kostnaðarstuðli.</span><span class="sxs-lookup"><span data-stu-id="ff2a7-133">**Description** – Enter the name and description of the cost factor.</span></span>
- <span data-ttu-id="ff2a7-134">**Upphafsdagur** og **Lokadagur** – Hægt er að nota þessa reiti til að takmarka kostnaðarstuðul fyrir tiltekið tímabil.</span><span class="sxs-lookup"><span data-stu-id="ff2a7-134">**Start date** and **End date** – You can use these fields to limit the cost factor for a specific date range.</span></span> <span data-ttu-id="ff2a7-135">Ef þessir reitir eru skildir eftir auðir gildir kostnaðarstuðullinn um óákveðinn tíma.</span><span class="sxs-lookup"><span data-stu-id="ff2a7-135">If you leave these fields blank, the cost factor is valid for an indefinite period.</span></span>
- <span data-ttu-id="ff2a7-136">**Virkur** – Segið til um hvort kostnaðarstuðull sé virkur.</span><span class="sxs-lookup"><span data-stu-id="ff2a7-136">**Active** – Indicate whether the cost factor is active.</span></span> <span data-ttu-id="ff2a7-137">DOM tekur aðeins virka kostnaðarstuðla til greina sem tengjast uppfyllingarsniði.</span><span class="sxs-lookup"><span data-stu-id="ff2a7-137">The DOM considers only active cost factors that are associated with the fulfillment profile.</span></span>
- <span data-ttu-id="ff2a7-138">**Fyrirtæki** – Tilgreinið lögaðila sem kostnaðarstuðull er skilgreindur fyrir.</span><span class="sxs-lookup"><span data-stu-id="ff2a7-138">**Company** – Specify the legal entity that the cost factor is configured for.</span></span> <span data-ttu-id="ff2a7-139">Allar línur útreikningsskilyrðis verður að vera fyrir sama lögaðilann.</span><span class="sxs-lookup"><span data-stu-id="ff2a7-139">All lines of the calculation criteria must be for the same legal entity.</span></span>
- <span data-ttu-id="ff2a7-140">**Afhendingarmátar** – Tilgreinið afhendingarmáta sem kostnaður er skilgreindur fyrir.</span><span class="sxs-lookup"><span data-stu-id="ff2a7-140">**Modes of delivery** – Specify the modes of delivery that the cost is configured for.</span></span>
- <span data-ttu-id="ff2a7-141">**Gerð útreiknings** – Tilgreinið hvernig reikna eigi kostnað fyrir tiltekinn afhendingarmáta.</span><span class="sxs-lookup"><span data-stu-id="ff2a7-141">**Calculation type** – Specify how the cost should be calculated for a specific mode of delivery.</span></span> <span data-ttu-id="ff2a7-142">Tvær gerðir útreiknings eru studdar:</span><span class="sxs-lookup"><span data-stu-id="ff2a7-142">Two calculation types are supported:</span></span>

    - <span data-ttu-id="ff2a7-143">**Fastur** – Flatur kostnaður er notaður fyrir afhendingarmáta.</span><span class="sxs-lookup"><span data-stu-id="ff2a7-143">**Fixed** – A flat cost is used for the mode of delivery.</span></span> <span data-ttu-id="ff2a7-144">Ef þessi útreikningsgerð er valin skilgreinir reiturinn **Kostnaður** flatan kostnað.</span><span class="sxs-lookup"><span data-stu-id="ff2a7-144">If you select this calculation type, the **Cost** field defines the flat cost.</span></span>
    - <span data-ttu-id="ff2a7-145">**Á hverja fjarlægðareiningu** – Kostnaður fyrir afhendingarmáta er reiknaður sem kostnaðarvirðið sem er skilgreint í reitnum **Kostnaður** margfaldað með vegalengdinni milli afhendingaraðseturs og staðsetningar.</span><span class="sxs-lookup"><span data-stu-id="ff2a7-145">**Per-distance unit** – The cost for the mode of delivery is calculated as the cost value that is specified in the **Cost** field times the distance between the delivery address and the locations.</span></span>

- <span data-ttu-id="ff2a7-146">**Kostnaður** – Tilgreinið kostnaðarvirði sem er notað í tengslum við reitinn **Gerð útreiknings** til að reikna út kostnað á afhendingarmáta.</span><span class="sxs-lookup"><span data-stu-id="ff2a7-146">**Cost** – Specify the cost value that is used in conjunction with the **Calculation type** field to compute the cost for a mode of delivery.</span></span>

#### <a name="cost-component-type--shipping-and-calculation-basis--tiered"></a><span data-ttu-id="ff2a7-147">Gerð kostnaðaríhlutar = sending og útreikningsgrunnur = lagskiptur</span><span class="sxs-lookup"><span data-stu-id="ff2a7-147">Cost component type = Shipping and Calculation basis = Tiered</span></span>

<span data-ttu-id="ff2a7-148">Ef samsetning kostnaðaríhlutar af gerðinni **Sending** og útreikningsgrunnurinn **Lagskiptur** er notuð byggist sendingarkostnaður fyrir afhendingarmáta annaðhvort á flötum kostnaði eða vegalengd.</span><span class="sxs-lookup"><span data-stu-id="ff2a7-148">If a combination of the **Shipping** cost component type and the **Tiered** calculation basis is used, the shipping cost for a mode of delivery is based on either a flat cost or distance.</span></span> <span data-ttu-id="ff2a7-149">Í þessari samsetningu byggist vegalengdin hins vegar á lagskiptu fjarlægðarbili.</span><span class="sxs-lookup"><span data-stu-id="ff2a7-149">However, in this combination, the distance is based on a tiered range of distances.</span></span>

<span data-ttu-id="ff2a7-150">Setja verður upp eftirfarandi reiti fyrir þessa samsetningu:</span><span class="sxs-lookup"><span data-stu-id="ff2a7-150">You must set up the following fields for this combination:</span></span>

- <span data-ttu-id="ff2a7-151">**Kostnaðarstuðull** – Færið inn einkvæmt kennimerki fyrir kostnaðarstuðul.</span><span class="sxs-lookup"><span data-stu-id="ff2a7-151">**Cost factor** – Enter a unique identifier for the cost factor.</span></span>
- <span data-ttu-id="ff2a7-152">**Lýsing** – Færið inn heiti og lýsingu á kostnaðarstuðli.</span><span class="sxs-lookup"><span data-stu-id="ff2a7-152">**Description** – Enter the name and description of the cost factor.</span></span>
- <span data-ttu-id="ff2a7-153">**Sjálfgefinn kostnaður** – Tilgreinið kostnað sem á að nota fyrir afhendingarmáta ef vegalengdin milli afhendingaraðseturs og staðsetningar fellur ekki undir neina af lagskiptu vegalengdunum fyrir afhendingarmáta.</span><span class="sxs-lookup"><span data-stu-id="ff2a7-153">**Default cost** – Specify the cost that should be used for a mode of delivery if the distance between the delivery address and the location doesn't fall into any of the tiered distances for the mode of delivery.</span></span>
- <span data-ttu-id="ff2a7-154">**Upphafsdagur** og **Lokadagur** – Hægt er að nota þessa reiti til að takmarka kostnaðarstuðul fyrir tiltekið tímabil.</span><span class="sxs-lookup"><span data-stu-id="ff2a7-154">**Start date** and **End date** – You can use these fields to limit the cost factor for a specific date range.</span></span> <span data-ttu-id="ff2a7-155">Ef þessir reitir eru skildir eftir auðir gildir kostnaðarstuðullinn um óákveðinn tíma.</span><span class="sxs-lookup"><span data-stu-id="ff2a7-155">If you leave these fields blank, the cost factor is valid for an indefinite period.</span></span>
- <span data-ttu-id="ff2a7-156">**Virkur** – Segið til um hvort kostnaðarstuðull sé virkur.</span><span class="sxs-lookup"><span data-stu-id="ff2a7-156">**Active** – Indicate whether the cost factor is active.</span></span> <span data-ttu-id="ff2a7-157">DOM tekur aðeins virka kostnaðarstuðla til greina sem tengjast uppfyllingarsniði.</span><span class="sxs-lookup"><span data-stu-id="ff2a7-157">The DOM considers only active cost factors that are associated with the fulfillment profile.</span></span>
- <span data-ttu-id="ff2a7-158">**Fyrirtæki** – Tilgreinið lögaðila sem kostnaðarstuðull er skilgreindur fyrir.</span><span class="sxs-lookup"><span data-stu-id="ff2a7-158">**Company** – Specify the legal entity that the cost factor is configured for.</span></span> <span data-ttu-id="ff2a7-159">Allar línur útreikningsskilyrðis verður að vera fyrir sama lögaðilann.</span><span class="sxs-lookup"><span data-stu-id="ff2a7-159">All lines of the calculation criteria must be for the same legal entity.</span></span>
- <span data-ttu-id="ff2a7-160">**Afhendingarmátar** – Tilgreinið afhendingarmáta sem kostnaður er skilgreindur fyrir.</span><span class="sxs-lookup"><span data-stu-id="ff2a7-160">**Modes of delivery** – Specify the modes of delivery that the cost is configured for.</span></span>
- <span data-ttu-id="ff2a7-161">**Tegund vegalengdar** – Tilgreinið hvort skilgreining á lagskiptri vegalengd sé fyrir flug eða akstur.</span><span class="sxs-lookup"><span data-stu-id="ff2a7-161">**Distance type** – Specify whether the tiered distance definition is an aerial distance or a road distance.</span></span>
- <span data-ttu-id="ff2a7-162">**Fjarlægðareiningar** – Tilgreinið einingu sem lagskipt vegalengd er mæld í.</span><span class="sxs-lookup"><span data-stu-id="ff2a7-162">**Distance units** – Specify the unit that the tiered distance is measured in.</span></span>
- <span data-ttu-id="ff2a7-163">**Fjarlægð frá** – Tilgreinið upphafsbil fyrir lagskipta vegalengd.</span><span class="sxs-lookup"><span data-stu-id="ff2a7-163">**Distance from** – Specify the start range for the tiered distance.</span></span>
- <span data-ttu-id="ff2a7-164">**Fjarlægð til** – Tilgreinið lokabil fyrir lagskipta vegalengd.</span><span class="sxs-lookup"><span data-stu-id="ff2a7-164">**Distance to** – Specify the end range for the tiered distance.</span></span>
- <span data-ttu-id="ff2a7-165">**Gerð útreiknings** – Tilgreinið hvernig reikna eigi kostnað fyrir tiltekinn afhendingarmáta og lagskipta vegalengd.</span><span class="sxs-lookup"><span data-stu-id="ff2a7-165">**Calculation type** – Specify how the cost should be calculated for a specific mode of delivery and tiered distance.</span></span> <span data-ttu-id="ff2a7-166">Tvær gerðir útreiknings eru studdar:</span><span class="sxs-lookup"><span data-stu-id="ff2a7-166">Two calculation types are supported:</span></span>

    - <span data-ttu-id="ff2a7-167">**Fastur** – Flatur kostnaður er notaður fyrir afhendingarmáta.</span><span class="sxs-lookup"><span data-stu-id="ff2a7-167">**Fixed** – A flat cost is used for the mode of delivery.</span></span> <span data-ttu-id="ff2a7-168">Ef þessi útreikningsgerð er valin skilgreinir reiturinn **Kostnaður** flatan kostnað.</span><span class="sxs-lookup"><span data-stu-id="ff2a7-168">If you select this calculation type, the **Cost** field defines the flat cost.</span></span>
    - <span data-ttu-id="ff2a7-169">**Á hverja fjarlægðareiningu** – Kostnaður fyrir afhendingarmáta og lagskipta vegalengd er reiknaður sem kostnaðarvirðið sem er skilgreint í reitnum **Kostnaður** margfaldað með vegalengdinni milli afhendingaraðseturs og staðsetningar.</span><span class="sxs-lookup"><span data-stu-id="ff2a7-169">**Per distance unit** – The cost for the mode of delivery and tiered distance is calculated as the cost value that is specified in the **Cost** field times the distance between the delivery address and the locations.</span></span>

- <span data-ttu-id="ff2a7-170">**Kostnaður** – Tilgreinið kostnaðarvirði sem er notað í tengslum við reitinn **Gerð útreiknings** til að reikna út kostnað á afhendingarmáta.</span><span class="sxs-lookup"><span data-stu-id="ff2a7-170">**Cost** – Specify the cost value that is used in conjunction with the **Calculation type** field to compute the cost for a mode of delivery.</span></span>

> [!NOTE]
> - <span data-ttu-id="ff2a7-171">Þegar lagskiptar vegalengdir eru skilgreindar sannprófar kerfið hvort vegalengdir vanti eða þær skarist á.</span><span class="sxs-lookup"><span data-stu-id="ff2a7-171">When you define tiered distances, the system validates that there are no missing or overlapping distances.</span></span>
> - <span data-ttu-id="ff2a7-172">Tegund vegalengdar sem er notuð fyrir afhendingarmáta verður að vera sú sama fyrir allar lagskiptu vegalengdirnar.</span><span class="sxs-lookup"><span data-stu-id="ff2a7-172">The distance type that is used for a mode of delivery must be the same across all the tiered distances.</span></span>

### <a name="other-cost-component-type"></a><span data-ttu-id="ff2a7-173">Önnur gerð kostnaðaríhlutar</span><span class="sxs-lookup"><span data-stu-id="ff2a7-173">Other cost component type</span></span>

<span data-ttu-id="ff2a7-174">Þessi hluti útskýrir hvernig á að setja upp hverja samsetningu fyrir sig fyrir kostnaðaríhlut af gerðinni **Annar** og aðra kostnaðargerð fyrir kostnað án sendingar.</span><span class="sxs-lookup"><span data-stu-id="ff2a7-174">This section explains how to set up each combination of the **Other** cost component type and an other cost type for non-shipping costs.</span></span> <span data-ttu-id="ff2a7-175">Þar er einnig útskýrt hvernig DOM-leysarinn notar hverja samsetningu.</span><span class="sxs-lookup"><span data-stu-id="ff2a7-175">It also explains how the DOM solver uses each combination.</span></span>

#### <a name="cost-component-type--other-and-other-cost-type--sales-order"></a><span data-ttu-id="ff2a7-176">Gerð kostnaðaríhlutar = annar og önnur kostnaðargerð = sölupöntun</span><span class="sxs-lookup"><span data-stu-id="ff2a7-176">Cost component type = Other and Other cost type = Sales order</span></span>

<span data-ttu-id="ff2a7-177">Samsetning fyrir kostnaðaríhlut af gerðinni **Annar** og annan kostnað af gerðinni **Sölupöntun** er notuð til að skilgreina kostnað án sendingar á stigi sölupöntunar.</span><span class="sxs-lookup"><span data-stu-id="ff2a7-177">A combination of the **Other** cost component type and the **Sales order** other cost type is used to define non-shipping costs at the sales order level.</span></span>

<span data-ttu-id="ff2a7-178">Setja verður upp eftirfarandi reiti fyrir þessa samsetningu:</span><span class="sxs-lookup"><span data-stu-id="ff2a7-178">You must set up the following fields for this combination:</span></span>

- <span data-ttu-id="ff2a7-179">**Kostnaðarstuðull** – Færið inn einkvæmt kennimerki fyrir kostnaðarstuðul.</span><span class="sxs-lookup"><span data-stu-id="ff2a7-179">**Cost factor** – Enter a unique identifier for the cost factor.</span></span>
- <span data-ttu-id="ff2a7-180">**Lýsing** – Færið inn heiti og lýsingu á kostnaðarstuðli.</span><span class="sxs-lookup"><span data-stu-id="ff2a7-180">**Description** – Enter the name and description of the cost factor.</span></span>
- <span data-ttu-id="ff2a7-181">**Upphafsdagur** og **Lokadagur** – Hægt er að nota þessa reiti til að takmarka kostnaðarstuðul fyrir tiltekið tímabil.</span><span class="sxs-lookup"><span data-stu-id="ff2a7-181">**Start date** and **End date** – You can use these fields to limit the cost factor for a specific date range.</span></span> <span data-ttu-id="ff2a7-182">Ef þessir reitir eru skildir eftir auðir gildir kostnaðarstuðullinn um óákveðinn tíma.</span><span class="sxs-lookup"><span data-stu-id="ff2a7-182">If you leave these fields blank, the cost factor is valid for an indefinite period.</span></span>
- <span data-ttu-id="ff2a7-183">**Virkur** – Segið til um hvort kostnaðarstuðull sé virkur.</span><span class="sxs-lookup"><span data-stu-id="ff2a7-183">**Active** – Indicate whether the cost factor is active.</span></span> <span data-ttu-id="ff2a7-184">DOM tekur aðeins virka kostnaðarstuðla til greina sem tengjast uppfyllingarsniði.</span><span class="sxs-lookup"><span data-stu-id="ff2a7-184">The DOM considers only active cost factors that are associated with the fulfillment profile.</span></span>
- <span data-ttu-id="ff2a7-185">**Kostnaður** – Tilgreinið kostnaðarvirði fyrir kostnað án sendingar á stigi sölupöntunar.</span><span class="sxs-lookup"><span data-stu-id="ff2a7-185">**Cost** – Specify the cost value for a non-shipping cost at the sales order level.</span></span>

#### <a name="cost-component-type--other-and-other-cost-type--sales-line"></a><span data-ttu-id="ff2a7-186">Gerð kostnaðaríhlutar = annar og önnur kostnaðargerð = sölulína</span><span class="sxs-lookup"><span data-stu-id="ff2a7-186">Cost component type = Other and Other cost type = Sales line</span></span>

<span data-ttu-id="ff2a7-187">Samsetning fyrir kostnaðaríhlut af gerðinni **Annar** og annan kostnað af gerðinni **Sölulína** er notuð til að skilgreina kostnað án sendingar á stigi sölulínu.</span><span class="sxs-lookup"><span data-stu-id="ff2a7-187">A combination of the **Other** cost component type and the **Sales line** other cost type is used to define non-shipping costs at the sales order line level.</span></span>

<span data-ttu-id="ff2a7-188">Setja verður upp eftirfarandi reiti fyrir þessa samsetningu:</span><span class="sxs-lookup"><span data-stu-id="ff2a7-188">You must set up the following fields for this combination:</span></span>

- <span data-ttu-id="ff2a7-189">**Kostnaðarstuðull** – Færið inn einkvæmt kennimerki fyrir kostnaðarstuðul.</span><span class="sxs-lookup"><span data-stu-id="ff2a7-189">**Cost factor** – Enter a unique identifier for the cost factor.</span></span>
- <span data-ttu-id="ff2a7-190">**Lýsing** – Færið inn heiti og lýsingu á kostnaðarstuðli.</span><span class="sxs-lookup"><span data-stu-id="ff2a7-190">**Description** – Enter the name and description of the cost factor.</span></span>
- <span data-ttu-id="ff2a7-191">**Upphafsdagur** og **Lokadagur** – Hægt er að nota þessa reiti til að takmarka kostnaðarstuðul fyrir tiltekið tímabil.</span><span class="sxs-lookup"><span data-stu-id="ff2a7-191">**Start date** and **End date** – You can use these fields to limit the cost factor for a specific date range.</span></span> <span data-ttu-id="ff2a7-192">Ef þessir reitir eru skildir eftir auðir gildir kostnaðarstuðullinn um óákveðinn tíma.</span><span class="sxs-lookup"><span data-stu-id="ff2a7-192">If you leave these fields blank, the cost factor is valid for an indefinite period.</span></span>
- <span data-ttu-id="ff2a7-193">**Virkur** – Segið til um hvort kostnaðarstuðull sé virkur.</span><span class="sxs-lookup"><span data-stu-id="ff2a7-193">**Active** – Indicate whether the cost factor is active.</span></span> <span data-ttu-id="ff2a7-194">DOM tekur aðeins virka kostnaðarstuðla til greina sem tengjast uppfyllingarsniði.</span><span class="sxs-lookup"><span data-stu-id="ff2a7-194">The DOM considers only active cost factors that are associated with the fulfillment profile.</span></span>
- <span data-ttu-id="ff2a7-195">**Kostnaður** – Tilgreinið kostnaðarvirði fyrir kostnað án sendingar á stigi sölupöntunarlínu.</span><span class="sxs-lookup"><span data-stu-id="ff2a7-195">**Cost** – Specify the cost value for a non-shipping cost at the sales order line level.</span></span>

#### <a name="cost-component-type--other-and-other-cost-type--location"></a><span data-ttu-id="ff2a7-196">Gerð kostnaðaríhlutar = annar og önnur kostnaðargerð = staðsetning</span><span class="sxs-lookup"><span data-stu-id="ff2a7-196">Cost component type = Other and Other cost type = Location</span></span>

<span data-ttu-id="ff2a7-197">Samsetning fyrir kostnaðaríhlut af gerðinni **Annar** og annan kostnað af gerðinni **Staðsetning** er notuð til að skilgreina kostnað án sendingar fyrir flokk staðsetninga eða eina staðsetningu.</span><span class="sxs-lookup"><span data-stu-id="ff2a7-197">A combination of the **Other** cost component type and the **Location** other cost type is used to define non-shipping costs for a group of locations or an individual location.</span></span>

<span data-ttu-id="ff2a7-198">Setja verður upp eftirfarandi reiti fyrir þessa samsetningu:</span><span class="sxs-lookup"><span data-stu-id="ff2a7-198">You must set up the following fields for this combination:</span></span>

- <span data-ttu-id="ff2a7-199">**Kostnaðarstuðull** – Færið inn einkvæmt kennimerki fyrir kostnaðarstuðul.</span><span class="sxs-lookup"><span data-stu-id="ff2a7-199">**Cost factor** – Enter a unique identifier for the cost factor.</span></span>
- <span data-ttu-id="ff2a7-200">**Lýsing** – Færið inn heiti og lýsingu á kostnaðarstuðli.</span><span class="sxs-lookup"><span data-stu-id="ff2a7-200">**Description** – Enter the name and description of the cost factor.</span></span>
- <span data-ttu-id="ff2a7-201">**Upphafsdagur** og **Lokadagur** – Hægt er að nota þessa reiti til að takmarka kostnaðarstuðul fyrir tiltekið tímabil.</span><span class="sxs-lookup"><span data-stu-id="ff2a7-201">**Start date** and **End date** – You can use these fields to limit the cost factor for a specific date range.</span></span> <span data-ttu-id="ff2a7-202">Ef þessir reitir eru skildir eftir auðir gildir kostnaðarstuðullinn um óákveðinn tíma.</span><span class="sxs-lookup"><span data-stu-id="ff2a7-202">If you leave these fields blank, the cost factor is valid for an indefinite period.</span></span>
- <span data-ttu-id="ff2a7-203">**Virkur** – Segið til um hvort kostnaðarstuðull sé virkur.</span><span class="sxs-lookup"><span data-stu-id="ff2a7-203">**Active** – Indicate whether the cost factor is active.</span></span> <span data-ttu-id="ff2a7-204">DOM tekur aðeins virka kostnaðarstuðla til greina sem tengjast uppfyllingarsniði.</span><span class="sxs-lookup"><span data-stu-id="ff2a7-204">The DOM considers only active cost factors that are associated with the fulfillment profile.</span></span>
- <span data-ttu-id="ff2a7-205">**Uppfyllingarflokkur** – Tilgreinið flokk staðsetninga sem kostnaður án sendingar er skilgreindur fyrir.</span><span class="sxs-lookup"><span data-stu-id="ff2a7-205">**Fulfillment group** – Specify the group of locations that the non-shipping cost is defined for.</span></span>
- <span data-ttu-id="ff2a7-206">**Uppfyllingarflokkur** – Tilgreinið staðsetningu sem kostnaður án sendingar er skilgreindur fyrir.</span><span class="sxs-lookup"><span data-stu-id="ff2a7-206">**Fulfillment location** – Specify the location that the non-shipping cost is defined for.</span></span>

    > [!NOTE]
    > <span data-ttu-id="ff2a7-207">Ekki er hægt að tilgreina uppfyllingarflokk og uppfyllingarstaðsetningu í sömu línunni fyrir útreikningsskilyrði sem byggir á staðsetningu.</span><span class="sxs-lookup"><span data-stu-id="ff2a7-207">You can't specify a fulfillment group and a fulfillment location on the same line for location-based calculation criteria.</span></span>

- <span data-ttu-id="ff2a7-208">**Kostnaður** – Tilgreinið kostnaðarvirði fyrir kostnað án sendingar á stigi uppfyllingarflokks eða uppfyllingarstaðsetningar.</span><span class="sxs-lookup"><span data-stu-id="ff2a7-208">**Cost** – Specify the cost value for a non-shipping cost at the fulfillment group level or fulfillment location level.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ff2a7-209">Til að DOM taki þennan kostnað til greina þegar hann er keyrður þarf að bæta kostnaðarstuðli við viðeigandi uppfyllingarsnið.</span><span class="sxs-lookup"><span data-stu-id="ff2a7-209">For DOM to consider these costs when it's run, you must add the cost factor to the relevant fulfillment profile.</span></span>