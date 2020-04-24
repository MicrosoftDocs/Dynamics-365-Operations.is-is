---
title: Afurðarvíddir
description: Það eru fjórar afurðavíddir - Litur, Skilgreining, Stærð og Stíll. Afurðavíddir eru sameinaðar í víddaflokka og víddaflokkum er úthlutað á afurðarsniðmát. Samsetning afurðavídda ræður til um það hvernig afurðarafbrigði eru skilgreind.
author: cvocph
manager: tfehr
ms.date: 08/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDimension, EcoResProductDimensionGroup, EcoResProductMasterDimension, RetailEcoResColor, RetailEcoResSize, RetailEcoResStyle
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations, Retail
ms.custom: 19171
ms.assetid: 81fa3709-4ab8-4fbf-9806-359892a05985
ms.search.region: Global
ms.search.industry: Retail
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f5e9b10fa18ada9534ce5e279d4f1f09973a802b
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/02/2020
ms.locfileid: "3208433"
---
# <a name="product-dimensions"></a><span data-ttu-id="497cd-105">Afurðarvíddir</span><span class="sxs-lookup"><span data-stu-id="497cd-105">Product dimensions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="497cd-106">Það eru fjórar afurðavíddir - Litur, Skilgreining, Stærð og Stíll.</span><span class="sxs-lookup"><span data-stu-id="497cd-106">There are four product dimensions -  Color, Configuration, Size and Style.</span></span> <span data-ttu-id="497cd-107">Afurðavíddir eru sameinaðar í víddaflokka og víddaflokkum er úthlutað á afurðarsniðmát.</span><span class="sxs-lookup"><span data-stu-id="497cd-107">You combine product dimensions in dimension groups and assign dimension groups to product masters.</span></span> <span data-ttu-id="497cd-108">Samsetning afurðavídda ræður til um það hvernig afurðarafbrigði eru skilgreind.</span><span class="sxs-lookup"><span data-stu-id="497cd-108">The combinations of product dimensions determine how product variants are defined.</span></span>

<span data-ttu-id="497cd-109">Afurðavíddir eru einkenni sem notaður er til að auðkenna afurðarafbrigði.</span><span class="sxs-lookup"><span data-stu-id="497cd-109">Product dimensions are characteristics that serve to identify a product variant.</span></span> <span data-ttu-id="497cd-110">Hægt er að nota samsetningu afurðavídda til að skilgreina afurðarafbrigði.</span><span class="sxs-lookup"><span data-stu-id="497cd-110">You can use combinations of product dimensions to define product variants.</span></span> <span data-ttu-id="497cd-111">Skilgreina verður minnst eina vídd afurðar fyrir afurðarsniðmát til að stofna afurðarafbrigði.</span><span class="sxs-lookup"><span data-stu-id="497cd-111">You must define at least one product dimension for a product master in order to create a product variant.</span></span>

## <a name="product-variants"></a><span data-ttu-id="497cd-112">Afurðarafbrigði</span><span class="sxs-lookup"><span data-stu-id="497cd-112">Product variants</span></span>

<span data-ttu-id="497cd-113">Afurðarafbrigði eru einnig nefndar vörur.</span><span class="sxs-lookup"><span data-stu-id="497cd-113">Product variants are also referred to as items.</span></span> <span data-ttu-id="497cd-114">Vara er áþreifanleg afurð sem er ekki það sama og þjónusta.</span><span class="sxs-lookup"><span data-stu-id="497cd-114">An item is a tangible product, which is not the same as a service.</span></span> <span data-ttu-id="497cd-115">Einnig hægt að skilgreina afurðarsniðmát með gerðinni Þjónusta.</span><span class="sxs-lookup"><span data-stu-id="497cd-115">It is also possible to define a product master with the Service type.</span></span> <span data-ttu-id="497cd-116">Með því að nota þjónustugerð, er hægt að tilgreina afurðarafbrigði sem innihalda þjónustu.</span><span class="sxs-lookup"><span data-stu-id="497cd-116">By using the Service type, you can specify product variants that include services.</span></span> <span data-ttu-id="497cd-117">Til dæmis er hægt að tilgreina afurðarsniðmát fyrir ráðgjafavinnu og afurða afbrigði fyrir vinnustöð sem er framkvæmd með hjá utanaðkomandi ráðgjöfum bókara og aðalbókara hjá utanaðkomandi ráðgjöfum.</span><span class="sxs-lookup"><span data-stu-id="497cd-117">For example, you can specify a product master for Consultancy work and product variants for work that is performed by senior consultants and junior consultants.</span></span>

## <a name="product-dimensions"></a><span data-ttu-id="497cd-118">Afurðarvíddir</span><span class="sxs-lookup"><span data-stu-id="497cd-118">Product dimensions</span></span>
<span data-ttu-id="497cd-119">Eftirfarandi afurðavíddir eru tiltækar: Afbrigði, Litur, Stærð og Stíll.</span><span class="sxs-lookup"><span data-stu-id="497cd-119">The following product dimensions are available: Configuration, Color, Size, and Style.</span></span> <span data-ttu-id="497cd-120">Hægt er að mynda afurðarafbrigði fyrir á grundvelli afurðarvíddargildi.</span><span class="sxs-lookup"><span data-stu-id="497cd-120">A product variant can be generated based on the product dimension values.</span></span>

<span data-ttu-id="497cd-121">Gildi afurðarvídda eins og Stærð, Lit og Stíl er hægt að stofna á í **Stærð**, **Litur** og **Stíll** síðum sem hægt er að komast í úr eftirfarandi staðsetningum: **Afurðarupplýsingastjórnun** &gt; **Uppsetningu** &gt; **Vídd og afbrigðaflokkar** &gt; **Stærðir/Litir/Stílar**.</span><span class="sxs-lookup"><span data-stu-id="497cd-121">Product dimensions values such as Size, Color and Style can be created on the **Size**, **Color** and **Style** pages, which can be accessed from the following locations: **Product information management** &gt; **Setup** &gt; **Dimension and variant Groups** &gt; **Sizes/Colors/Styles**.</span></span> <span data-ttu-id="497cd-122">Afurðarvíddargildi fyrir skilgreiningarvíddir eru yfirleitt stofnaðar með afurðaafbrigðastilli eða afurðarafbrigðastillis sem byggir á víddum.</span><span class="sxs-lookup"><span data-stu-id="497cd-122">Product dimension values for the Configuration dimension are typically created using either the Product configurator or the Dimension-based configurator.</span></span> <span data-ttu-id="497cd-123">Vöruvíddir er einnig hægt að stofnað og þeim viðhaldið í **afurðarvíddir** síðu, sem fæst frá eftirfarandi staðsetningum:</span><span class="sxs-lookup"><span data-stu-id="497cd-123">Product dimensions can also be created and maintained on the **Product dimensions** page, which can be accessed from the following locations:</span></span>
-   <span data-ttu-id="497cd-124">Smellið á **Upplýsingar um afurðarstjórnun** &gt; **Afurðir** &gt; **Afurðarsniðmát**.</span><span class="sxs-lookup"><span data-stu-id="497cd-124">Click **Product information management** &gt; **Products** &gt; **Product masters**.</span></span> <span data-ttu-id="497cd-125">Á **Aðgerðasvæði** skal smella á **Afurðarvíddir**.</span><span class="sxs-lookup"><span data-stu-id="497cd-125">On the **Action Pane**, click **Product dimensions**.</span></span>
-   <span data-ttu-id="497cd-126">Smellið á **Upplýsingastjórnun afurða** &gt; **Afurðir** &gt; **Allar afurðir og afurðarsniðmát**.</span><span class="sxs-lookup"><span data-stu-id="497cd-126">Click **Product information management** &gt; **Products** &gt; **All products and product masters**.</span></span> <span data-ttu-id="497cd-127">Veljið afurðarsniðmát.</span><span class="sxs-lookup"><span data-stu-id="497cd-127">Select a product master.</span></span> <span data-ttu-id="497cd-128">Á **Aðgerðasvæði** skal smella á **Afurðarvíddir**.</span><span class="sxs-lookup"><span data-stu-id="497cd-128">On the **Action Pane**, click **Product dimensions**.</span></span>
-   <span data-ttu-id="497cd-129">Smellið á **Upplýsingastjórnun afurðar** &gt; **Útgefnar afurðir**.</span><span class="sxs-lookup"><span data-stu-id="497cd-129">Click **Product information management** &gt; **Released products**.</span></span> <span data-ttu-id="497cd-130">Veljið afurðarsniðmát.</span><span class="sxs-lookup"><span data-stu-id="497cd-130">Select a product master.</span></span> <span data-ttu-id="497cd-131">Í **Aðgerðasvæði** er smellt á **Afurð**.</span><span class="sxs-lookup"><span data-stu-id="497cd-131">On the **Action Pane**, click **Product**.</span></span> <span data-ttu-id="497cd-132">Í reitnum **afurðarsniðmát** flokki, skal velja **afurðarvíddir**.</span><span class="sxs-lookup"><span data-stu-id="497cd-132">In the **Product master** group, click **Product dimensions**.</span></span>

<span data-ttu-id="497cd-133">Númer vöruvíddasamsetningar sem hægt er að stofna fyrir vöru er takmörkuð af fjölda afurð mögulegar samsetningar.</span><span class="sxs-lookup"><span data-stu-id="497cd-133">The number of variants that you can create for an item is limited by the number of possible product dimension combinations.</span></span>

| <span data-ttu-id="497cd-134">**Ábending**</span><span class="sxs-lookup"><span data-stu-id="497cd-134">**Tip**</span></span>                                                                                                                                              |
|------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="497cd-135">Þegar þú notar afurð á til dæmis pöntunarlínu velurðu afurðavíddir til að tilgreina afurðarafbrigði sem á að vinna með.</span><span class="sxs-lookup"><span data-stu-id="497cd-135">When you use a product on, for example, an order line, you select the product dimensions to identify the product variant that you want to work with.</span></span> |

## <a name="example"></a><span data-ttu-id="497cd-136">Dæmi</span><span class="sxs-lookup"><span data-stu-id="497cd-136">Example</span></span>
<span data-ttu-id="497cd-137">Fyrirtæki selur denim-gallabuxur.</span><span class="sxs-lookup"><span data-stu-id="497cd-137">A company sells denim jeans.</span></span> <span data-ttu-id="497cd-138">Varan, gallabuxur, notar lit og stærð afurðarvíddirnar.</span><span class="sxs-lookup"><span data-stu-id="497cd-138">The item, Jeans, uses the Color and Size product dimensions.</span></span> <span data-ttu-id="497cd-139">Gallabuxurnar eru til í þremur mismunandi litum og sex mismunandi stærðum.</span><span class="sxs-lookup"><span data-stu-id="497cd-139">The jeans are sold in three different colors and six different sizes.</span></span> <span data-ttu-id="497cd-140">Litir: Blár, Svartur, brúnn Stærðir: XS, S, M, L, XL, XXL Ekki allar stærðir eru tiltækar í öllum þremur litum.</span><span class="sxs-lookup"><span data-stu-id="497cd-140">Colors: Blue, Black, Brown Sizes: XS, S, M, L, XL, XXL Not all sizes are available in all the three colors.</span></span> <span data-ttu-id="497cd-141">Ef allar samsetningar voru tiltæk, hún myndi stofna 18 mismunandi gerðir af gallabuxur.</span><span class="sxs-lookup"><span data-stu-id="497cd-141">If all combinations were available, it would create 18 different types of jeans.</span></span> <span data-ttu-id="497cd-142">Í þessu dæmi eru aðeins eftirfarandi níu vara afbrigði samsetningar framleitt.</span><span class="sxs-lookup"><span data-stu-id="497cd-142">In this example, only the following nine product variant combinations are produced.</span></span>

| <span data-ttu-id="497cd-143">Litur</span><span class="sxs-lookup"><span data-stu-id="497cd-143">Color</span></span> | <span data-ttu-id="497cd-144">Stærð</span><span class="sxs-lookup"><span data-stu-id="497cd-144">Size</span></span> |
|-------|------|
| <span data-ttu-id="497cd-145">Blátt</span><span class="sxs-lookup"><span data-stu-id="497cd-145">Blue</span></span>  | <span data-ttu-id="497cd-146">XS</span><span class="sxs-lookup"><span data-stu-id="497cd-146">XS</span></span>   |
| <span data-ttu-id="497cd-147">Blátt</span><span class="sxs-lookup"><span data-stu-id="497cd-147">Blue</span></span>  | <span data-ttu-id="497cd-148">L</span><span class="sxs-lookup"><span data-stu-id="497cd-148">S</span></span>    |
| <span data-ttu-id="497cd-149">Blátt</span><span class="sxs-lookup"><span data-stu-id="497cd-149">Blue</span></span>  | <span data-ttu-id="497cd-150">M</span><span class="sxs-lookup"><span data-stu-id="497cd-150">M</span></span>    |
| <span data-ttu-id="497cd-151">Svart</span><span class="sxs-lookup"><span data-stu-id="497cd-151">Black</span></span> | <span data-ttu-id="497cd-152">M</span><span class="sxs-lookup"><span data-stu-id="497cd-152">M</span></span>    |
| <span data-ttu-id="497cd-153">Svart</span><span class="sxs-lookup"><span data-stu-id="497cd-153">Black</span></span> | <span data-ttu-id="497cd-154">L</span><span class="sxs-lookup"><span data-stu-id="497cd-154">L</span></span>    |
| <span data-ttu-id="497cd-155">Svart</span><span class="sxs-lookup"><span data-stu-id="497cd-155">Black</span></span> | <span data-ttu-id="497cd-156">XL</span><span class="sxs-lookup"><span data-stu-id="497cd-156">XL</span></span>   |
| <span data-ttu-id="497cd-157">Brúnt</span><span class="sxs-lookup"><span data-stu-id="497cd-157">Brown</span></span> | <span data-ttu-id="497cd-158">L</span><span class="sxs-lookup"><span data-stu-id="497cd-158">L</span></span>    |
| <span data-ttu-id="497cd-159">Brúnt</span><span class="sxs-lookup"><span data-stu-id="497cd-159">Brown</span></span> | <span data-ttu-id="497cd-160">XL</span><span class="sxs-lookup"><span data-stu-id="497cd-160">XL</span></span>   |
| <span data-ttu-id="497cd-161">Brúnt</span><span class="sxs-lookup"><span data-stu-id="497cd-161">Brown</span></span> | <span data-ttu-id="497cd-162">XXL</span><span class="sxs-lookup"><span data-stu-id="497cd-162">XXL</span></span>  |





