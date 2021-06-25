---
title: Nafnakerfi afurðarafbrigðisnúmera og -nafna
description: Þetta efnisatriði lýsir því hvernig hægt er að setja upp nafnakerfi afurðarnúmers til að skipta út föstu sniði [Númer afurðarsniðmáts - Skilgreining - Stærð - Litur - Stíll].
author: roxanadiaconu
ms.date: 11/03/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResNomenclature, EcoResProductDimensionGroup, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelDetails
audience: Application User
ms.reviewer: kamaybac
ms.custom: 220104
ms.assetid: 3fe69fb7-5c32-423c-98a8-2f53186cda68
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: edab3420cbd39539358c03fe4d6b3646433f8ec5
ms.sourcegitcommit: ff09736563d3cd2bc74c7664edd1767b218401cb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/04/2021
ms.locfileid: "6190161"
---
# <a name="nomenclature-of-product-variant-numbers-and-names"></a><span data-ttu-id="ebcb8-103">Nafnakerfi afurðarafbrigðisnúmera og -nafna</span><span class="sxs-lookup"><span data-stu-id="ebcb8-103">Nomenclature of product variant numbers and names</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ebcb8-104">Þetta efnisatriði lýsir því hvernig hægt er að setja upp nafnakerfi afurðarnúmers til að skipta út föstu sniði [Númer afurðarsniðmáts - Skilgreining - Stærð - Litur - Stíll].</span><span class="sxs-lookup"><span data-stu-id="ebcb8-104">This topic describes how you can set up a product number nomenclature to replace the fixed [Product master number - Configuration - Size - Color - Style] format.</span></span> <span data-ttu-id="ebcb8-105">Nýja nafnakerfið er með markað snið sem tekur til númers afurðarsniðmátsins, virku afurðavíddanna og skiltákna texta að eigin vali.</span><span class="sxs-lookup"><span data-stu-id="ebcb8-105">The new nomenclature has a targeted format that includes the product master number, active product dimensions, and text delimiters of your choice.</span></span> <span data-ttu-id="ebcb8-106">Einnig er hægt að stofna nafnakerfi fyrir afurðaheiti.</span><span class="sxs-lookup"><span data-stu-id="ebcb8-106">You can also create a nomenclature for product names.</span></span> <span data-ttu-id="ebcb8-107">Loks er hægt að búa til nafnakerfi til að auðkenna grunnstillingar sem eru stofnaðar af skorðumiðuðum afurðarafbrigðastilli.</span><span class="sxs-lookup"><span data-stu-id="ebcb8-107">Finally, you can build a nomenclature to identify configurations that are created by the constraint-based product configurator.</span></span> <span data-ttu-id="ebcb8-108">Þessum nafnakerfi geta innihaldið eigindir að eigin vali.</span><span class="sxs-lookup"><span data-stu-id="ebcb8-108">These nomenclatures can contain attributes of your choice.</span></span>

<span data-ttu-id="ebcb8-109">Ný nafnakerfi fyrir afurðarafbrigðanúmer og afurðarafbrigðaheiti gera þér kleift að taka með hluta auðkennanna fyrir afurðarafbrigði.</span><span class="sxs-lookup"><span data-stu-id="ebcb8-109">The new nomenclatures for product variant numbers and product variant names let you include segments in the identifiers for product variants.</span></span> <span data-ttu-id="ebcb8-110">Slíkir hluta geta falið í sér afurðarsniðmát, númer og heiti, auðkenni afurðavídda og heiti, númeraraðir, textafasta og eigindir.</span><span class="sxs-lookup"><span data-stu-id="ebcb8-110">These segments can include the product master number and name, product dimension IDs and names, number sequences, text constants, and attributes.</span></span> <span data-ttu-id="ebcb8-111">Þessi virkni leyfir þér að finna á fljótan hátt tilteknar afurðarafbrigði þegar þú stofnar sölupöntun eða innkaupapöntun.</span><span class="sxs-lookup"><span data-stu-id="ebcb8-111">This functionality lets you quickly find a specific product variant when you create a sales order or a purchase order.</span></span> <span data-ttu-id="ebcb8-112">Nafnakerfi fyrir bæði afurðarafbrigðanúmer og afurðarafbrigðaheiti eru stofnuð með því að nota síðuna **Nafnakerfi afurðar**.</span><span class="sxs-lookup"><span data-stu-id="ebcb8-112">You create nomenclatures for both product variant numbers and product variant names by using the **Product nomenclature** page.</span></span> <span data-ttu-id="ebcb8-113">Til að opna þessa síðu er smellt á **afurðaupplýsingastjórnun,** &gt; **Uppsetning**.</span><span class="sxs-lookup"><span data-stu-id="ebcb8-113">To open this page, click **Product information management** &gt; **Setup**.</span></span>

## <a name="nomenclature-of-predefined-product-variants"></a><span data-ttu-id="ebcb8-114">Nafnakerfi fyrirframskilgreindra afurðarafbrigða</span><span class="sxs-lookup"><span data-stu-id="ebcb8-114">Nomenclature of predefined product variants</span></span>
<span data-ttu-id="ebcb8-115">Afurðarafbrigði eru myndaðar fyrir afurðarsniðmát í samræmi við eina af þremur afbrigðistækni:</span><span class="sxs-lookup"><span data-stu-id="ebcb8-115">Product variants are generated for product masters according to one of three configuration technologies:</span></span>

-   <span data-ttu-id="ebcb8-116">Forskilgreint afbrigði</span><span class="sxs-lookup"><span data-stu-id="ebcb8-116">Predefined variants</span></span>
-   <span data-ttu-id="ebcb8-117">Skorðumiðað</span><span class="sxs-lookup"><span data-stu-id="ebcb8-117">Constraint-based</span></span>
-   <span data-ttu-id="ebcb8-118">Víddarmiðað</span><span class="sxs-lookup"><span data-stu-id="ebcb8-118">Dimension-based</span></span>

<span data-ttu-id="ebcb8-119">Hvert afurðarafbrigði hefur númer og heiti og nafnakerfi auðkennins afurðarafbrigðis leyfir þér að velja hlutana sem verða hafðir með í hverju númeri eða heiti afurðarafbrigðis.</span><span class="sxs-lookup"><span data-stu-id="ebcb8-119">Each product variant has a number and a name, and the product variant identification nomenclatures let you select the segments that will be included in each product variant number or name.</span></span> <span data-ttu-id="ebcb8-120">Hægt að velja eftirfarandi hluta á síðunni **Nafnakerfi afurðar**.</span><span class="sxs-lookup"><span data-stu-id="ebcb8-120">You can select the following segments on the **Product nomenclature** page:</span></span>

-   <span data-ttu-id="ebcb8-121">Númer afurðarsniðmáts</span><span class="sxs-lookup"><span data-stu-id="ebcb8-121">Product master number</span></span>
-   <span data-ttu-id="ebcb8-122">Heiti afurðarsniðmáts</span><span class="sxs-lookup"><span data-stu-id="ebcb8-122">Product master name</span></span>
-   <span data-ttu-id="ebcb8-123">Gildi númeraraðar</span><span class="sxs-lookup"><span data-stu-id="ebcb8-123">Number sequence value</span></span>
-   <span data-ttu-id="ebcb8-124">Textafasti</span><span class="sxs-lookup"><span data-stu-id="ebcb8-124">Text constant</span></span>
-   <span data-ttu-id="ebcb8-125">Afurðarvíddir</span><span class="sxs-lookup"><span data-stu-id="ebcb8-125">Product dimensions</span></span>
    -   <span data-ttu-id="ebcb8-126">Veljið skilgreiningarkenni eða -heiti</span><span class="sxs-lookup"><span data-stu-id="ebcb8-126">Configuration ID or name</span></span>
    -   <span data-ttu-id="ebcb8-127">Kenni eða heiti litar</span><span class="sxs-lookup"><span data-stu-id="ebcb8-127">Color ID or name</span></span>
    -   <span data-ttu-id="ebcb8-128">Kenni eða heiti stærðar</span><span class="sxs-lookup"><span data-stu-id="ebcb8-128">Size ID or name</span></span>
    -   <span data-ttu-id="ebcb8-129">Kenni eða heiti stílsniðs</span><span class="sxs-lookup"><span data-stu-id="ebcb8-129">Style ID or name</span></span>

<span data-ttu-id="ebcb8-130">Eftir að auðkenni nafnakerfis afurðarafbrigðis er skilgreint, er hægt að tengja það við afurðarvíddarflokk.</span><span class="sxs-lookup"><span data-stu-id="ebcb8-130">After you define a product variant identification number nomenclature, you can associate it with a product dimension group.</span></span> <span data-ttu-id="ebcb8-131">Þá verður öllum afurðarsniðmátum sem vísa til þessa afurðarvíddarflokks úthlutað númerum afurðarafbrigða í samræmi við nafnakerfið.</span><span class="sxs-lookup"><span data-stu-id="ebcb8-131">All product masters that reference this product dimension group will then be assigned product variant numbers according to the nomenclature.</span></span> <span data-ttu-id="ebcb8-132">Nafnakerfi fyrir afurðaafbrigðaheiti er hins vegar ekki hægt að tengja við afurðavíddaflokka.</span><span class="sxs-lookup"><span data-stu-id="ebcb8-132">However, product variant name nomenclatures can't be associated with product dimension groups.</span></span> <span data-ttu-id="ebcb8-133">Einnig má tengja nafnakerfi fyrir auðkenni afurðarafbrigðis beint við aðalsniðmát.</span><span class="sxs-lookup"><span data-stu-id="ebcb8-133">You can also assign a product variant identification nomenclature directly to a product master.</span></span> <span data-ttu-id="ebcb8-134">Í því rtilviki verður afurðarafbrigðim sem tilheyra afurðasniðmátinu úthlutað afurðarafbrigðanúmerum og -heitum í samræmi við nafnakerfin.</span><span class="sxs-lookup"><span data-stu-id="ebcb8-134">In this case, the product variants that belong to the product master will be assigned product variant numbers and names according to the nomenclatures.</span></span>

### <a name="example"></a><span data-ttu-id="ebcb8-135">Dæmi</span><span class="sxs-lookup"><span data-stu-id="ebcb8-135">Example</span></span>

<span data-ttu-id="ebcb8-136">Stuttermabolur (TS1234) er framleiddur í þremur stærðum (S, M, L) fjórum litum (Rauður, Grænn, Blár, Gulur) og tveimur sniðum (pólóbolur, vaffhálsmál).</span><span class="sxs-lookup"><span data-stu-id="ebcb8-136">A T-shirt (TS1234) is produced in three sizes (S, M, L), four colors (Red, Green, Blue, Yellow), and two styles (Polo, V).</span></span> <span data-ttu-id="ebcb8-137">Þar af leiðir að 24 afurðarafbrigði eru möguleg (= 3 × 4 × 2).</span><span class="sxs-lookup"><span data-stu-id="ebcb8-137">Therefore, 24 product variants are possible (= 3 × 4 × 2).</span></span> <span data-ttu-id="ebcb8-138">Stofnað er nafnakerfi fyrir afurðarafbrigðisnúmer sem hefur eftirfarandi hluta:</span><span class="sxs-lookup"><span data-stu-id="ebcb8-138">You create a product variant number nomenclature that has the following segments:</span></span>

1.  <span data-ttu-id="ebcb8-139">Númer afurðarsniðmáts</span><span class="sxs-lookup"><span data-stu-id="ebcb8-139">Product master number</span></span>
2.  <span data-ttu-id="ebcb8-140">Textafasti: "-"</span><span class="sxs-lookup"><span data-stu-id="ebcb8-140">Text constant: "-"</span></span>
3.  <span data-ttu-id="ebcb8-141">Litur</span><span class="sxs-lookup"><span data-stu-id="ebcb8-141">Color</span></span>
4.  <span data-ttu-id="ebcb8-142">Textafasti: "-"</span><span class="sxs-lookup"><span data-stu-id="ebcb8-142">Text constant: "-"</span></span>
5.  <span data-ttu-id="ebcb8-143">Stærð</span><span class="sxs-lookup"><span data-stu-id="ebcb8-143">Size</span></span>
6.  <span data-ttu-id="ebcb8-144">Textafasti: "-"</span><span class="sxs-lookup"><span data-stu-id="ebcb8-144">Text constant: "-"</span></span>
7.  <span data-ttu-id="ebcb8-145">Stíll</span><span class="sxs-lookup"><span data-stu-id="ebcb8-145">Style</span></span>

<span data-ttu-id="ebcb8-146">Í þessu tilviki er afurðarafbrigðisnúmer fyrir rauðan, lítill pólóbol fyrir TS1234-Red-Small-Polo.</span><span class="sxs-lookup"><span data-stu-id="ebcb8-146">In this case, the product variant number for a red, small, polo T-shirt will be TS1234-Red-Small-Polo.</span></span>

## <a name="nomenclature-of-constraint-based-configurations"></a><span data-ttu-id="ebcb8-147">Nafnakerfi skorðuskilgreininga</span><span class="sxs-lookup"><span data-stu-id="ebcb8-147">Nomenclature of constraint-based configurations</span></span>
<span data-ttu-id="ebcb8-148">Fyrir skorðuskilgreiningar er hægt að stofna sérhæft nafnakerfi fyrir skilgreiningu afurðarvídda.</span><span class="sxs-lookup"><span data-stu-id="ebcb8-148">For constraint-based configurations, you can create a dedicated nomenclature for the configuration product dimension.</span></span> <span data-ttu-id="ebcb8-149">Hægt að velja eftirfarandi hluta á síðunni **Nafnakerfi afurðar**.</span><span class="sxs-lookup"><span data-stu-id="ebcb8-149">You can select the following segments on the **Product nomenclature** page:</span></span>

-   <span data-ttu-id="ebcb8-150">Gildi númeraraðar</span><span class="sxs-lookup"><span data-stu-id="ebcb8-150">Number sequence value</span></span>
-   <span data-ttu-id="ebcb8-151">Textafasti</span><span class="sxs-lookup"><span data-stu-id="ebcb8-151">Text constant</span></span>
-   <span data-ttu-id="ebcb8-152">Eigindargildi</span><span class="sxs-lookup"><span data-stu-id="ebcb8-152">Attribute value</span></span>

<span data-ttu-id="ebcb8-153">Hver þáttur í afbrigðalíkan afurðar getur haft sitt eigið skilgreinda nafnakerfi.</span><span class="sxs-lookup"><span data-stu-id="ebcb8-153">Each component in a product configuration model can have its own configuration nomenclature.</span></span> <span data-ttu-id="ebcb8-154">Aðeins má nota eigindir sem tilheyra íhlutnum.</span><span class="sxs-lookup"><span data-stu-id="ebcb8-154">Only attributes that belong to the component can be used.</span></span> <span data-ttu-id="ebcb8-155">Eigindir úr undiríhlutir eða notendakröfur eru ekki nothæfar.</span><span class="sxs-lookup"><span data-stu-id="ebcb8-155">Attributes from subcomponents or user requirements can't be used.</span></span>

### <a name="example"></a><span data-ttu-id="ebcb8-156">Dæmi</span><span class="sxs-lookup"><span data-stu-id="ebcb8-156">Example</span></span>

<span data-ttu-id="ebcb8-157">Afbrigðalíkan afurðar hefur rótaríhlut með tvær eigindir:</span><span class="sxs-lookup"><span data-stu-id="ebcb8-157">A product configuration model has a root component that has two attributes:</span></span>

-   <span data-ttu-id="ebcb8-158">Efni (Plast, viður, Stáli)</span><span class="sxs-lookup"><span data-stu-id="ebcb8-158">Material (Plastic, Wood, Steel)</span></span>
-   <span data-ttu-id="ebcb8-159">Lengd (10... 100)</span><span class="sxs-lookup"><span data-stu-id="ebcb8-159">Length (10...100)</span></span>

<span data-ttu-id="ebcb8-160">Stofnað er nafnakerfi skilgreiningar sem inniheldur eftirfarandi hluta:</span><span class="sxs-lookup"><span data-stu-id="ebcb8-160">You create a configuration nomenclature that has the following segments:</span></span>

1.  <span data-ttu-id="ebcb8-161">Eigindargildi: Efni</span><span class="sxs-lookup"><span data-stu-id="ebcb8-161">Attribute value: Material</span></span>
2.  <span data-ttu-id="ebcb8-162">Textafasti: "AAA"</span><span class="sxs-lookup"><span data-stu-id="ebcb8-162">Text constant: "AAA"</span></span>
3.  <span data-ttu-id="ebcb8-163">Eigindargildi: Lengd</span><span class="sxs-lookup"><span data-stu-id="ebcb8-163">Attribute value: Length</span></span>

<span data-ttu-id="ebcb8-164">Í þessu tilfelli er skilgreiningarkenni fyrir viðarefni sem er 78 á lengd WoodAAA78.</span><span class="sxs-lookup"><span data-stu-id="ebcb8-164">In this case, the configuration ID for wood material that has a length of 78 will be WoodAAA78.</span></span>

## <a name="nomenclature-of-dimension-based-configurations"></a><span data-ttu-id="ebcb8-165">Víddarbyggðrar skilgreiningar Nafnakerfis</span><span class="sxs-lookup"><span data-stu-id="ebcb8-165">Nomenclature of dimension-based configurations</span></span>
<span data-ttu-id="ebcb8-166">Fyrir skorðuskilgreiningar er hægt að stofna sérhæft nafnakerfi fyrir skilgreiningu afurðarvídda.</span><span class="sxs-lookup"><span data-stu-id="ebcb8-166">For dimension-based configurations, you can create a dedicated nomenclature for the configuration product dimension.</span></span> <span data-ttu-id="ebcb8-167">Hægt að velja eftirfarandi hluta á síðunni **Nafnakerfi afurðar**.</span><span class="sxs-lookup"><span data-stu-id="ebcb8-167">You can select the following segments on the **Product nomenclature** page:</span></span>

-   <span data-ttu-id="ebcb8-168">Gildi númeraraðar</span><span class="sxs-lookup"><span data-stu-id="ebcb8-168">Number sequence value</span></span>
-   <span data-ttu-id="ebcb8-169">Textafasti</span><span class="sxs-lookup"><span data-stu-id="ebcb8-169">Text constant</span></span>
-   <span data-ttu-id="ebcb8-170">Afbrigðisflokksvara</span><span class="sxs-lookup"><span data-stu-id="ebcb8-170">Configuration group item</span></span>

<span data-ttu-id="ebcb8-171">Nafnakerfi skilgreiningar má skilgreina fyrir uppskrift (BOM).</span><span class="sxs-lookup"><span data-stu-id="ebcb8-171">You can define a configuration nomenclature for a bill of materials (BOM).</span></span>

### <a name="example"></a><span data-ttu-id="ebcb8-172">Dæmi</span><span class="sxs-lookup"><span data-stu-id="ebcb8-172">Example</span></span>

<span data-ttu-id="ebcb8-173">Uppskrift hefur fjórar uppskriftalínur sem er skipt í tvo skilgreiningarflokka:</span><span class="sxs-lookup"><span data-stu-id="ebcb8-173">A BOM has four BOM lines that are divided into two configuration groups:</span></span>

-   <span data-ttu-id="ebcb8-174">Uppskriftarlínu: M0007, Staðlaða Cabinet</span><span class="sxs-lookup"><span data-stu-id="ebcb8-174">BOM line: M0007, Standard cabinet</span></span>
    -   <span data-ttu-id="ebcb8-175">Afbrigðaflokkur: Cabinet</span><span class="sxs-lookup"><span data-stu-id="ebcb8-175">Configuration group: Cabinet</span></span>
-   <span data-ttu-id="ebcb8-176">Uppskriftarlínu: M0008, háklassa cabinet</span><span class="sxs-lookup"><span data-stu-id="ebcb8-176">BOM line: M0008, High end cabinet</span></span>
    -   <span data-ttu-id="ebcb8-177">Afbrigðaflokkur: Cabinet</span><span class="sxs-lookup"><span data-stu-id="ebcb8-177">Configuration group: Cabinet</span></span>
-   <span data-ttu-id="ebcb8-178">Uppskriftarlínu: M0021, klæði framgrills</span><span class="sxs-lookup"><span data-stu-id="ebcb8-178">BOM line: M0021, Front grill cloth</span></span>
    -   <span data-ttu-id="ebcb8-179">Skilgreiningaflokkur: framgrill</span><span class="sxs-lookup"><span data-stu-id="ebcb8-179">Configuration group: Front grill</span></span>
-   <span data-ttu-id="ebcb8-180">Uppskriftarlínu: M0022, framgrill stál</span><span class="sxs-lookup"><span data-stu-id="ebcb8-180">BOM line: M0022, Front grill metal</span></span>
    -   <span data-ttu-id="ebcb8-181">Skilgreiningaflokkur: framgrill</span><span class="sxs-lookup"><span data-stu-id="ebcb8-181">Configuration group: Front grill</span></span>

<span data-ttu-id="ebcb8-182">Stofnað er nafnakerfi skilgreiningar sem inniheldur eftirfarandi hluta:</span><span class="sxs-lookup"><span data-stu-id="ebcb8-182">You create a configuration nomenclature that has the following segments:</span></span>

1.  <span data-ttu-id="ebcb8-183">Afbrigðaflokkur: Cabinet</span><span class="sxs-lookup"><span data-stu-id="ebcb8-183">Configuration group: Cabinet</span></span>
2.  <span data-ttu-id="ebcb8-184">Textafasti: "&"</span><span class="sxs-lookup"><span data-stu-id="ebcb8-184">Text constant: "&"</span></span>
3.  <span data-ttu-id="ebcb8-185">Skilgreiningaflokkur: framgrill</span><span class="sxs-lookup"><span data-stu-id="ebcb8-185">Configuration group: Front grill</span></span>

<span data-ttu-id="ebcb8-186">Í þessu tilfelli er skilgreiningarkenni fyrirstaðlaðan skáp sem er með framhlið úr tauklæði M0007&M0021.</span><span class="sxs-lookup"><span data-stu-id="ebcb8-186">In this case, the configuration ID for a standard cabinet that has a cloth front grill will be M0007&M0021.</span></span>

## <a name="nomenclature-for-a-combination-of-product-variants-and-configurations"></a><span data-ttu-id="ebcb8-187">Nafnakerfi fyrir samsetningu afurðarafbrigða og skilgreininga</span><span class="sxs-lookup"><span data-stu-id="ebcb8-187">Nomenclature for a combination of product variants and configurations</span></span>
<span data-ttu-id="ebcb8-188">Þegar þú notar annaðhvort tæknina skorðumiðaðar eða víddarbyggðar skilgreiningar til að skilgreina afurðarafbrigði fyrir afurðarsniðmát, geta afurðarsniðmát fengið númer afurðarafbrigðis sem innihalda nafnakerfið úr vídd skilgreiningarinnar.</span><span class="sxs-lookup"><span data-stu-id="ebcb8-188">When you use either the constraint-based configuration technology or the dimension-based configuration technology to configure product variants for a product master, the product variant numbers of the product variants can include the nomenclature from the configuration dimension.</span></span> <span data-ttu-id="ebcb8-189">Fylgja skal þessum skrefum til að skilgreina afbrigði.</span><span class="sxs-lookup"><span data-stu-id="ebcb8-189">Follow these steps to configure variants.</span></span>

1.  <span data-ttu-id="ebcb8-190">Skilgreina á nafnakerfi afurðarafbrigðisnúmers sem er með skilgreiningarvídd á síðunni **nafnakerfi afurðar**.</span><span class="sxs-lookup"><span data-stu-id="ebcb8-190">On the **Product nomenclature** page, define a product variant number nomenclature that includes the configuration dimension.</span></span>
2.  <span data-ttu-id="ebcb8-191">Úthluta þessa nafnakerfi á afurðarvíddarflokk með skilgreiningarvídd.</span><span class="sxs-lookup"><span data-stu-id="ebcb8-191">Assign the nomenclature to a product dimension group that has the configuration dimension.</span></span>
3.  <span data-ttu-id="ebcb8-192">Skilgreina nafnakerfi skilgreiningar fyrir íhlutina eða uppskriftirnar sem verða notaðar til að skilgreina afurðarafbrigðin.</span><span class="sxs-lookup"><span data-stu-id="ebcb8-192">Define a configuration nomenclature for the components or BOMs that will be used to configure the product variants.</span></span>

<span data-ttu-id="ebcb8-193">Einnig er hægt að stofna nafnakerfi fyrir afurðarafbrigðisheitin.</span><span class="sxs-lookup"><span data-stu-id="ebcb8-193">You can also create nomenclatures for the product variant names.</span></span> <span data-ttu-id="ebcb8-194">Heiti afurðarafbrgiða er hægt að skilgreina þannig að þau innihaldi kenni eða heiti skilgreiningarinnar.</span><span class="sxs-lookup"><span data-stu-id="ebcb8-194">The product variant names can be configured to include the configuration ID or name.</span></span>

### <a name="example-for-constraint-based-configurations"></a><span data-ttu-id="ebcb8-195">Dæmi um skorðuskilgreiningar</span><span class="sxs-lookup"><span data-stu-id="ebcb8-195">Example for constraint-based configurations</span></span>

<span data-ttu-id="ebcb8-196">Í þessu dæmi er notað nafnakerfi afurðarafbrigðisnúmers sem samanstendur úr eftirfarandi hlutum:</span><span class="sxs-lookup"><span data-stu-id="ebcb8-196">For this example, you use a product variant number nomenclature that consists of the following segments:</span></span>

1.  <span data-ttu-id="ebcb8-197">Númer afurðarsniðmáts</span><span class="sxs-lookup"><span data-stu-id="ebcb8-197">Product master number</span></span>
2.  <span data-ttu-id="ebcb8-198">Textafasti "\_"</span><span class="sxs-lookup"><span data-stu-id="ebcb8-198">Text constant "\_"</span></span>
3.  <span data-ttu-id="ebcb8-199">Afbrigði</span><span class="sxs-lookup"><span data-stu-id="ebcb8-199">Configuration</span></span>

<span data-ttu-id="ebcb8-200">Nafnakerfi skilgreiningar inniheldur eftirfarandi hluta:</span><span class="sxs-lookup"><span data-stu-id="ebcb8-200">The configuration nomenclature consists of the following segments:</span></span>

1.  <span data-ttu-id="ebcb8-201">Eigindargildi: Efni</span><span class="sxs-lookup"><span data-stu-id="ebcb8-201">Attribute value: Material</span></span>
2.  <span data-ttu-id="ebcb8-202">Textafasti: "AAA"</span><span class="sxs-lookup"><span data-stu-id="ebcb8-202">Text constant: "AAA"</span></span>
3.  <span data-ttu-id="ebcb8-203">Eigindargildi: Lengd</span><span class="sxs-lookup"><span data-stu-id="ebcb8-203">Attribute value: Length</span></span>

<span data-ttu-id="ebcb8-204">Hægt er að færa inn eftirfarandi gildi fyrir hluta:</span><span class="sxs-lookup"><span data-stu-id="ebcb8-204">You enter the following values for segments:</span></span>

-   <span data-ttu-id="ebcb8-205">Númer afurðarsniðmáts = **M0099**</span><span class="sxs-lookup"><span data-stu-id="ebcb8-205">Product master number = **M0099**</span></span>
-   <span data-ttu-id="ebcb8-206">Efni = **Plast**</span><span class="sxs-lookup"><span data-stu-id="ebcb8-206">Material = **Plastic**</span></span>
-   <span data-ttu-id="ebcb8-207">Lengd = **12**</span><span class="sxs-lookup"><span data-stu-id="ebcb8-207">Length = **12**</span></span>

<span data-ttu-id="ebcb8-208">Í þessu tilviki verður afurðarafbrigðisnúmerið M0099\_PlasticAAA12.</span><span class="sxs-lookup"><span data-stu-id="ebcb8-208">In this case, the product variant number will be M0099\_PlasticAAA12.</span></span>

### <a name="example-for-dimension-based-configurations"></a><span data-ttu-id="ebcb8-209">Dæmi um víddarbyggðar skilgreiningar</span><span class="sxs-lookup"><span data-stu-id="ebcb8-209">Example for dimension-based configurations</span></span>

<span data-ttu-id="ebcb8-210">Í þessu dæmi er notað nafnakerfi afurðarafbrigðisnúmers sem samanstendur úr eftirfarandi hlutum:</span><span class="sxs-lookup"><span data-stu-id="ebcb8-210">For this example, you use a product variant number nomenclature that consists of the following segments:</span></span>

1.  <span data-ttu-id="ebcb8-211">Númer afurðarsniðmáts</span><span class="sxs-lookup"><span data-stu-id="ebcb8-211">Product master number</span></span>
2.  <span data-ttu-id="ebcb8-212">Textafasti "//"</span><span class="sxs-lookup"><span data-stu-id="ebcb8-212">Text constant "//"</span></span>
3.  <span data-ttu-id="ebcb8-213">Afbrigði</span><span class="sxs-lookup"><span data-stu-id="ebcb8-213">Configuration</span></span>

<span data-ttu-id="ebcb8-214">Nafnakerfi skilgreiningar inniheldur eftirfarandi hluta:</span><span class="sxs-lookup"><span data-stu-id="ebcb8-214">The configuration nomenclature consists of the following segments:</span></span>

1.  <span data-ttu-id="ebcb8-215">Afbrigðaflokkur: Cabinet</span><span class="sxs-lookup"><span data-stu-id="ebcb8-215">Configuration group: Cabinet</span></span>
2.  <span data-ttu-id="ebcb8-216">Textafasti: "&"</span><span class="sxs-lookup"><span data-stu-id="ebcb8-216">Text constant: "&"</span></span>
3.  <span data-ttu-id="ebcb8-217">Skilgreiningaflokkur: framgrill</span><span class="sxs-lookup"><span data-stu-id="ebcb8-217">Configuration group: Front grill</span></span>

<span data-ttu-id="ebcb8-218">Hægt er að færa inn eftirfarandi gildi fyrir hluta:</span><span class="sxs-lookup"><span data-stu-id="ebcb8-218">You enter the following values for segments:</span></span>

-   <span data-ttu-id="ebcb8-219">Númer afurðarsniðmáts = **D0123**</span><span class="sxs-lookup"><span data-stu-id="ebcb8-219">Product master number = **D0123**</span></span>
-   <span data-ttu-id="ebcb8-220">Skápur = **M0008**</span><span class="sxs-lookup"><span data-stu-id="ebcb8-220">Cabinet = **M0008**</span></span>
-   <span data-ttu-id="ebcb8-221">Framhlið = **M0022**</span><span class="sxs-lookup"><span data-stu-id="ebcb8-221">Front grill = **M0022**</span></span>

<span data-ttu-id="ebcb8-222">Í þessu tilviki verður afurðarafbrigðisnúmerið D0123//M0008&M0022.</span><span class="sxs-lookup"><span data-stu-id="ebcb8-222">In this case, the product variant number will be D0123//M0008&M0022.</span></span>

## <a name="numbering-conflicts"></a><span data-ttu-id="ebcb8-223">Árekstrar númera</span><span class="sxs-lookup"><span data-stu-id="ebcb8-223">Numbering conflicts</span></span>
<span data-ttu-id="ebcb8-224">Mögulegt er að setja upp afurð nafnakerfi afurðarafbrigðisnúmers sem leiðir ekki til einkvæmra númera afurðarafbrigða.</span><span class="sxs-lookup"><span data-stu-id="ebcb8-224">In some cases, a product variant number nomenclature that you set up might not produce unique product variant numbers.</span></span> <span data-ttu-id="ebcb8-225">Til dæmis verða númer afurðarafbrigða ekki einnkvæm ef ein virk afurðarvídd er ekki innifalin í nafnakerfi fyrir afurðarsniðmát sem notar forskilgreinda tækni til skilgreiningar afbrigða.</span><span class="sxs-lookup"><span data-stu-id="ebcb8-225">For example, the product variant numbers won't be unique if one active product dimension isn't included in the nomenclature for a product master that uses the predefined variant configuration technology.</span></span> <span data-ttu-id="ebcb8-226">Aðferðin til að meðhöndla árekstra er breytileg eftir tækni við skilgreiningu.</span><span class="sxs-lookup"><span data-stu-id="ebcb8-226">The way that you handle conflicts varies, depending on the configuration technology.</span></span>

### <a name="predefined-variants"></a><span data-ttu-id="ebcb8-227">Forskilgreint afbrigði</span><span class="sxs-lookup"><span data-stu-id="ebcb8-227">Predefined variants</span></span>

<span data-ttu-id="ebcb8-228">Villa mun eiga sér stað ef reynt er að handvirkt eða sjálfkrafa mynda afurðarafbrigði þar sem eitt eða fleiri afurðarafbrigði endar á því að hafa sama númer afurðarafbrigðis.</span><span class="sxs-lookup"><span data-stu-id="ebcb8-228">An error occurs if you try to manually create or automatically generate product variants, and more than one product variant ends up with the same product variant number.</span></span> <span data-ttu-id="ebcb8-229">Til að forðast slíkt ætti frekar að nota allar virkar afurðarvíddar í afurðavíddaflokki.</span><span class="sxs-lookup"><span data-stu-id="ebcb8-229">To avoid this scenario, you should use all active product dimensions in the product dimension group.</span></span> <span data-ttu-id="ebcb8-230">Einnig er hægt að hafa með númeraröð til að tryggja enn betur að afurðarafbrigðisnúmerin séu einkvæm.</span><span class="sxs-lookup"><span data-stu-id="ebcb8-230">Alternatively, include a number sequence to help guarantee that the product variant numbers are unique.</span></span>

### <a name="constraint-based-configurations"></a><span data-ttu-id="ebcb8-231">Skorðuskilgreiningar</span><span class="sxs-lookup"><span data-stu-id="ebcb8-231">Constraint-based configurations</span></span>

<span data-ttu-id="ebcb8-232">Allt eftir nafnakerfinu getur kerfið reynt að úthluta númeri afurðarafbrigðis sem ekki er einkvæmt á skilgreiningu.</span><span class="sxs-lookup"><span data-stu-id="ebcb8-232">Depending on the nomenclature, the system might try to assign a non-unique product variant number to a configuration.</span></span> <span data-ttu-id="ebcb8-233">Í slíku tilfelli mun kerfið nota númeraröð fyrir vídd skilgreiningarvíddina sem númer afurðarafbrigðis í staðinn. Ef það gerist, mun viðvörun berast.</span><span class="sxs-lookup"><span data-stu-id="ebcb8-233">In this case, the system uses the number sequence for the configuration dimension as the product variant number instead, and you receive a warning.</span></span> <span data-ttu-id="ebcb8-234">Til að forðast slíkt ætti að taka með nógu margar eigindir í nafnakerfið til að stuðla að því að tryggja einkvæm afurðarafbrigðanúmer.</span><span class="sxs-lookup"><span data-stu-id="ebcb8-234">To avoid this scenario, you should include enough attributes in the nomenclature to help guarantee unique product variant numbers.</span></span> <span data-ttu-id="ebcb8-235">Einnig ætti að ganga úr skugga um að kveikt sé á valkostinum **Endurnota** fyrir íhlutinn.</span><span class="sxs-lookup"><span data-stu-id="ebcb8-235">You should also make sure that the **Reuse** option is turned on for the component.</span></span>

### <a name="dimension-based-configurations"></a><span data-ttu-id="ebcb8-236">Víddaskilgreiningar</span><span class="sxs-lookup"><span data-stu-id="ebcb8-236">Dimension-based configurations</span></span>

<span data-ttu-id="ebcb8-237">Á einu þrefi skilgreiningarferlisins leggur kerfið til skilgreiningargildi í samræmi við nafnakerfið.</span><span class="sxs-lookup"><span data-stu-id="ebcb8-237">During one step of the configuration process, the system suggests a configuration value according to the nomenclature.</span></span> <span data-ttu-id="ebcb8-238">Í þessu skrefi geturðu Handvirkt breytt gildi skilgreiningarinnar.</span><span class="sxs-lookup"><span data-stu-id="ebcb8-238">In this step, you can manually change the configuration value.</span></span> <span data-ttu-id="ebcb8-239">Þegar skilgreining er vistuð, mun kerfið athuga hvort gildi skilgreiningar er einkvæmt.</span><span class="sxs-lookup"><span data-stu-id="ebcb8-239">When you save the configuration, the system verifies that the configuration value is unique.</span></span> <span data-ttu-id="ebcb8-240">Ef gildið sem fært er inn er ekki einkvæmt verða send villuboð.</span><span class="sxs-lookup"><span data-stu-id="ebcb8-240">If the value that you entered isn't unique, you receive an error message.</span></span> <span data-ttu-id="ebcb8-241">Færa þarf inn gildi einkvæmrar skilgreiningar til að vista skilgreininguna.</span><span class="sxs-lookup"><span data-stu-id="ebcb8-241">To save the configuration, you must enter a unique configuration value.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ebcb8-242">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="ebcb8-242">Additional resources</span></span>

[<span data-ttu-id="ebcb8-243">Stofna nafnakerfi afurðarnúmers fyrir fyrirframskilgreind afurðarafbrigði</span><span class="sxs-lookup"><span data-stu-id="ebcb8-243">Create a product number nomenclature for predefined product variants</span></span>](tasks/create-product-number-nomenclature-predefined-variants-2016-11.md)

[<span data-ttu-id="ebcb8-244">Stofna nafnakerfi afurðarafbrigðis fyrir skilgreind afurðarafbrigði</span><span class="sxs-lookup"><span data-stu-id="ebcb8-244">Create a product number nomenclature for configured product variants</span></span>](tasks/create-product-number-nomenclature-product-variants_2016_11.md)



[!INCLUDE[footer-include](../../includes/footer-banner.md)]