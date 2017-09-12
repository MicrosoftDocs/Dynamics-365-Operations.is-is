---
title: "Nafnakerfi afurðarafbrigðisnúmera og -nafna"
description: "Þetta efnisatriði lýsir því hvernig hægt er að setja upp nafnakerfi afurðarnúmers til að skipta út föstu sniði [Númer afurðarsniðmáts - Skilgreining - Stærð - Litur - Stíll]. Nýja nafnakerfið er með markað snið sem tekur til númers afurðarsniðmátsins, virku afurðavíddanna og skiltákna texta að eigin vali. Einnig er hægt að stofna nafnakerfi fyrir afurðaheiti. Loks er hægt að búa til nafnakerfi til að auðkenna grunnstillingar sem eru stofnaðar af skorðumiðuðum afurðarafbrigðastilli. Þessum nafnakerfi geta innihaldið eigindir að eigin vali."
author: roxanadiaconu
manager: AnnBe
ms.date: 05/10/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: EcoResNomenclature, EcoResProductDimensionGroup, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelDetails
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 220104
ms.assetid: 3fe69fb7-5c32-423c-98a8-2f53186cda68
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.dyn365.ops.intro: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: d1a9ced00d8dc09e59512056392a250a76ba5b97
ms.contentlocale: is-is
ms.lasthandoff: 08/29/2017

---

# <a name="nomenclature-of-product-variant-numbers-and-names"></a><span data-ttu-id="9ff7d-107">Nafnakerfi afurðarafbrigðisnúmera og -nafna</span><span class="sxs-lookup"><span data-stu-id="9ff7d-107">Nomenclature of product variant numbers and names</span></span>

<span data-ttu-id="9ff7d-108">Þetta efnisatriði lýsir því hvernig hægt er að setja upp nafnakerfi afurðarnúmers til að skipta út föstu sniði [Númer afurðarsniðmáts - Skilgreining - Stærð - Litur - Stíll].</span><span class="sxs-lookup"><span data-stu-id="9ff7d-108">This topic describes how you can set up a product number nomenclature to replace the fixed [Product master number - Configuration - Size - Color - Style] format.</span></span> <span data-ttu-id="9ff7d-109">Nýja nafnakerfið er með markað snið sem tekur til númers afurðarsniðmátsins, virku afurðavíddanna og skiltákna texta að eigin vali.</span><span class="sxs-lookup"><span data-stu-id="9ff7d-109">The new nomenclature has a targeted format that includes the product master number, active product dimensions, and text delimiters of your choice.</span></span> <span data-ttu-id="9ff7d-110">Einnig er hægt að stofna nafnakerfi fyrir afurðaheiti.</span><span class="sxs-lookup"><span data-stu-id="9ff7d-110">You can also create a nomenclature for product names.</span></span> <span data-ttu-id="9ff7d-111">Loks er hægt að búa til nafnakerfi til að auðkenna grunnstillingar sem eru stofnaðar af skorðumiðuðum afurðarafbrigðastilli.</span><span class="sxs-lookup"><span data-stu-id="9ff7d-111">Finally, you can build a nomenclature to identify configurations that are created by the constraint-based product configurator.</span></span> <span data-ttu-id="9ff7d-112">Þessum nafnakerfi geta innihaldið eigindir að eigin vali.</span><span class="sxs-lookup"><span data-stu-id="9ff7d-112">These nomenclatures can contain attributes of your choice.</span></span>

<span data-ttu-id="9ff7d-113">Ný nafnakerfi fyrir afurðarafbrigðanúmer og afurðarafbrigðaheiti gera þér kleift að taka með hluta auðkennanna fyrir afurðarafbrigði.</span><span class="sxs-lookup"><span data-stu-id="9ff7d-113">The new nomenclatures for product variant numbers and product variant names let you include segments in the identifiers for product variants.</span></span> <span data-ttu-id="9ff7d-114">Slíkir hluta geta falið í sér afurðarsniðmát, númer og heiti, auðkenni afurðavídda og heiti, númeraraðir, textafasta og eigindir.</span><span class="sxs-lookup"><span data-stu-id="9ff7d-114">These segments can include the product master number and name, product dimension IDs and names, number sequences, text constants, and attributes.</span></span> <span data-ttu-id="9ff7d-115">Þessi virkni leyfir þér að finna á fljótan hátt tilteknar afurðarafbrigði þegar þú stofnar sölupöntun eða innkaupapöntun.</span><span class="sxs-lookup"><span data-stu-id="9ff7d-115">This functionality lets you quickly find a specific product variant when you create a sales order or a purchase order.</span></span> <span data-ttu-id="9ff7d-116">Nafnakerfi fyrir bæði afurðarafbrigðanúmer og afurðarafbrigðaheiti eru stofnuð með því að nota síðuna **Nafnakerfi afurðar**.</span><span class="sxs-lookup"><span data-stu-id="9ff7d-116">You create nomenclatures for both product variant numbers and product variant names by using the **Product nomenclature** page.</span></span> <span data-ttu-id="9ff7d-117">Til að opna þessa síðu er smellt á **afurðaupplýsingastjórnun,** &gt; **Uppsetning**.</span><span class="sxs-lookup"><span data-stu-id="9ff7d-117">To open this page, click **Product information management** &gt; **Setup**.</span></span>

## <a name="nomenclature-of-predefined-product-variants"></a><span data-ttu-id="9ff7d-118">Nafnakerfi fyrirframskilgreindra afurðarafbrigða</span><span class="sxs-lookup"><span data-stu-id="9ff7d-118">Nomenclature of predefined product variants</span></span>
<span data-ttu-id="9ff7d-119">Afurðarafbrigði eru myndaðar fyrir afurðarsniðmát í samræmi við eina af þremur afbrigðistækni:</span><span class="sxs-lookup"><span data-stu-id="9ff7d-119">Product variants are generated for product masters according to one of three configuration technologies:</span></span>

-   <span data-ttu-id="9ff7d-120">Forskilgreint afbrigði</span><span class="sxs-lookup"><span data-stu-id="9ff7d-120">Predefined variants</span></span>
-   <span data-ttu-id="9ff7d-121">Skorðumiðað</span><span class="sxs-lookup"><span data-stu-id="9ff7d-121">Constraint-based</span></span>
-   <span data-ttu-id="9ff7d-122">Víddarmiðað</span><span class="sxs-lookup"><span data-stu-id="9ff7d-122">Dimension-based</span></span>

<span data-ttu-id="9ff7d-123">Hvert afurðarafbrigði hefur númer og heiti og nafnakerfi auðkennins afurðarafbrigðis leyfir þér að velja hlutana sem verða hafðir með í hverju númeri eða heiti afurðarafbrigðis.</span><span class="sxs-lookup"><span data-stu-id="9ff7d-123">Each product variant has a number and a name, and the product variant identification nomenclatures let you select the segments that will be included in each product variant number or name.</span></span> <span data-ttu-id="9ff7d-124">Hægt að velja eftirfarandi hluta á síðunni **Nafnakerfi afurðar**.</span><span class="sxs-lookup"><span data-stu-id="9ff7d-124">You can select the following segments on the **Product nomenclature** page:</span></span>

-   <span data-ttu-id="9ff7d-125">Númer afurðarsniðmáts</span><span class="sxs-lookup"><span data-stu-id="9ff7d-125">Product master number</span></span>
-   <span data-ttu-id="9ff7d-126">Heiti afurðarsniðmáts</span><span class="sxs-lookup"><span data-stu-id="9ff7d-126">Product master name</span></span>
-   <span data-ttu-id="9ff7d-127">Gildi númeraraðar</span><span class="sxs-lookup"><span data-stu-id="9ff7d-127">Number sequence value</span></span>
-   <span data-ttu-id="9ff7d-128">Textafasti</span><span class="sxs-lookup"><span data-stu-id="9ff7d-128">Text constant</span></span>
-   <span data-ttu-id="9ff7d-129">Afurðarvíddir</span><span class="sxs-lookup"><span data-stu-id="9ff7d-129">Product dimensions</span></span>
    -   <span data-ttu-id="9ff7d-130">Veljið skilgreiningarkenni eða -heiti</span><span class="sxs-lookup"><span data-stu-id="9ff7d-130">Configuration ID or name</span></span>
    -   <span data-ttu-id="9ff7d-131">Kenni eða heiti litar</span><span class="sxs-lookup"><span data-stu-id="9ff7d-131">Color ID or name</span></span>
    -   <span data-ttu-id="9ff7d-132">Kenni eða heiti stærðar</span><span class="sxs-lookup"><span data-stu-id="9ff7d-132">Size ID or name</span></span>
    -   <span data-ttu-id="9ff7d-133">Kenni eða heiti stílsniðs</span><span class="sxs-lookup"><span data-stu-id="9ff7d-133">Style ID or name</span></span>

<span data-ttu-id="9ff7d-134">Eftir að auðkenni nafnakerfis afurðarafbrigðis er skilgreint, er hægt að tengja það við afurðarvíddarflokk.</span><span class="sxs-lookup"><span data-stu-id="9ff7d-134">After you define a product variant identification number nomenclature, you can associate it with a product dimension group.</span></span> <span data-ttu-id="9ff7d-135">Þá verður öllum afurðarsniðmátum sem vísa til þessa afurðarvíddarflokks úthlutað númerum afurðarafbrigða í samræmi við nafnakerfið.</span><span class="sxs-lookup"><span data-stu-id="9ff7d-135">All product masters that reference this product dimension group will then be assigned product variant numbers according to the nomenclature.</span></span> <span data-ttu-id="9ff7d-136">Nafnakerfi fyrir afurðaafbrigðaheiti er hins vegar ekki hægt að tengja við afurðavíddaflokka.</span><span class="sxs-lookup"><span data-stu-id="9ff7d-136">However, product variant name nomenclatures can't be associated with product dimension groups.</span></span> <span data-ttu-id="9ff7d-137">Einnig má tengja nafnakerfi fyrir auðkenni afurðarafbrigðis beint við aðalsniðmát.</span><span class="sxs-lookup"><span data-stu-id="9ff7d-137">You can also assign a product variant identification nomenclature directly to a product master.</span></span> <span data-ttu-id="9ff7d-138">Í því rtilviki verður afurðarafbrigðim sem tilheyra afurðasniðmátinu úthlutað afurðarafbrigðanúmerum og -heitum í samræmi við nafnakerfin.</span><span class="sxs-lookup"><span data-stu-id="9ff7d-138">In this case, the product variants that belong to the product master will be assigned product variant numbers and names according to the nomenclatures.</span></span>

### <a name="example"></a><span data-ttu-id="9ff7d-139">Dæmi</span><span class="sxs-lookup"><span data-stu-id="9ff7d-139">Example</span></span>

<span data-ttu-id="9ff7d-140">Stuttermabolur (TS1234) er framleiddur í þremur stærðum (S, M, L) fjórum litum (Rauður, Grænn, Blár, Gulur) og tveimur sniðum (pólóbolur, vaffhálsmál).</span><span class="sxs-lookup"><span data-stu-id="9ff7d-140">A T-shirt (TS1234) is produced in three sizes (S, M, L), four colors (Red, Green, Blue, Yellow), and two styles (Polo, V).</span></span> <span data-ttu-id="9ff7d-141">Þar af leiðir að 24 afurðarafbrigði eru möguleg (= 3 × 4 × 2).</span><span class="sxs-lookup"><span data-stu-id="9ff7d-141">Therefore, 24 product variants are possible (= 3 × 4 × 2).</span></span> <span data-ttu-id="9ff7d-142">Stofnað er nafnakerfi fyrir afurðarafbrigðisnúmer sem hefur eftirfarandi hluta:</span><span class="sxs-lookup"><span data-stu-id="9ff7d-142">You create a product variant number nomenclature that has the following segments:</span></span>

1.  <span data-ttu-id="9ff7d-143">Númer afurðarsniðmáts</span><span class="sxs-lookup"><span data-stu-id="9ff7d-143">Product master number</span></span>
2.  <span data-ttu-id="9ff7d-144">Textafasti: "-"</span><span class="sxs-lookup"><span data-stu-id="9ff7d-144">Text constant: "-"</span></span>
3.  <span data-ttu-id="9ff7d-145">Litur</span><span class="sxs-lookup"><span data-stu-id="9ff7d-145">Color</span></span>
4.  <span data-ttu-id="9ff7d-146">Textafasti: "-"</span><span class="sxs-lookup"><span data-stu-id="9ff7d-146">Text constant: "-"</span></span>
5.  <span data-ttu-id="9ff7d-147">Stærð</span><span class="sxs-lookup"><span data-stu-id="9ff7d-147">Size</span></span>
6.  <span data-ttu-id="9ff7d-148">Textafasti: "-"</span><span class="sxs-lookup"><span data-stu-id="9ff7d-148">Text constant: "-"</span></span>
7.  <span data-ttu-id="9ff7d-149">Stíll</span><span class="sxs-lookup"><span data-stu-id="9ff7d-149">Style</span></span>

<span data-ttu-id="9ff7d-150">Í þessu tilviki er afurðarafbrigðisnúmer fyrir rauðan, lítill pólóbol fyrir TS1234-Red-Small-Polo.</span><span class="sxs-lookup"><span data-stu-id="9ff7d-150">In this case, the product variant number for a red, small, polo T-shirt will be TS1234-Red-Small-Polo.</span></span>

## <a name="nomenclature-of-constraintbased-configurations"></a><span data-ttu-id="9ff7d-151">Nafnakerfi skorðuskilgreininga</span><span class="sxs-lookup"><span data-stu-id="9ff7d-151">Nomenclature of constraintbased configurations</span></span>
<span data-ttu-id="9ff7d-152">Fyrir skorðuskilgreiningar er hægt að stofna sérhæft nafnakerfi fyrir skilgreiningu afurðarvídda.</span><span class="sxs-lookup"><span data-stu-id="9ff7d-152">For constraint-based configurations, you can create a dedicated nomenclature for the configuration product dimension.</span></span> <span data-ttu-id="9ff7d-153">Hægt að velja eftirfarandi hluta á síðunni **Nafnakerfi afurðar**.</span><span class="sxs-lookup"><span data-stu-id="9ff7d-153">You can select the following segments on the **Product nomenclature** page:</span></span>

-   <span data-ttu-id="9ff7d-154">Gildi númeraraðar</span><span class="sxs-lookup"><span data-stu-id="9ff7d-154">Number sequence value</span></span>
-   <span data-ttu-id="9ff7d-155">Textafasti</span><span class="sxs-lookup"><span data-stu-id="9ff7d-155">Text constant</span></span>
-   <span data-ttu-id="9ff7d-156">Eigindargildi</span><span class="sxs-lookup"><span data-stu-id="9ff7d-156">Attribute value</span></span>

<span data-ttu-id="9ff7d-157">Hver þáttur í afbrigðalíkan afurðar getur haft sitt eigið skilgreinda nafnakerfi.</span><span class="sxs-lookup"><span data-stu-id="9ff7d-157">Each component in a product configuration model can have its own configuration nomenclature.</span></span> <span data-ttu-id="9ff7d-158">Aðeins má nota eigindir sem tilheyra íhlutnum.</span><span class="sxs-lookup"><span data-stu-id="9ff7d-158">Only attributes that belong to the component can be used.</span></span> <span data-ttu-id="9ff7d-159">Eigindir úr undiríhlutir eða notendakröfur eru ekki nothæfar.</span><span class="sxs-lookup"><span data-stu-id="9ff7d-159">Attributes from subcomponents or user requirements can't be used.</span></span>

### <a name="example"></a><span data-ttu-id="9ff7d-160">Dæmi</span><span class="sxs-lookup"><span data-stu-id="9ff7d-160">Example</span></span>

<span data-ttu-id="9ff7d-161">Afbrigðalíkan afurðar hefur rótaríhlut með tvær eigindir:</span><span class="sxs-lookup"><span data-stu-id="9ff7d-161">A product configuration model has a root component that has two attributes:</span></span>

-   <span data-ttu-id="9ff7d-162">Efni (Plast, viður, Stáli)</span><span class="sxs-lookup"><span data-stu-id="9ff7d-162">Material (Plastic, Wood, Steel)</span></span>
-   <span data-ttu-id="9ff7d-163">Lengd (10... 100)</span><span class="sxs-lookup"><span data-stu-id="9ff7d-163">Length (10...100)</span></span>

<span data-ttu-id="9ff7d-164">Stofnað er nafnakerfi skilgreiningar sem inniheldur eftirfarandi hluta:</span><span class="sxs-lookup"><span data-stu-id="9ff7d-164">You create a configuration nomenclature that has the following segments:</span></span>

1.  <span data-ttu-id="9ff7d-165">Eigindargildi: Efni</span><span class="sxs-lookup"><span data-stu-id="9ff7d-165">Attribute value: Material</span></span>
2.  <span data-ttu-id="9ff7d-166">Textafasti: "AAA"</span><span class="sxs-lookup"><span data-stu-id="9ff7d-166">Text constant: "AAA"</span></span>
3.  <span data-ttu-id="9ff7d-167">Eigindargildi: Lengd</span><span class="sxs-lookup"><span data-stu-id="9ff7d-167">Attribute value: Length</span></span>

<span data-ttu-id="9ff7d-168">Í þessu tilfelli er skilgreiningarkenni fyrir viðarefni sem er 78 á lengd WoodAAA78.</span><span class="sxs-lookup"><span data-stu-id="9ff7d-168">In this case, the configuration ID for wood material that has a length of 78 will be WoodAAA78.</span></span>

## <a name="nomenclature-of-dimensionbased-configurations"></a><span data-ttu-id="9ff7d-169">Víddarbyggðrar skilgreiningar Nafnakerfis</span><span class="sxs-lookup"><span data-stu-id="9ff7d-169">Nomenclature of dimensionbased configurations</span></span>
<span data-ttu-id="9ff7d-170">Fyrir skorðuskilgreiningar er hægt að stofna sérhæft nafnakerfi fyrir skilgreiningu afurðarvídda.</span><span class="sxs-lookup"><span data-stu-id="9ff7d-170">For dimension-based configurations, you can create a dedicated nomenclature for the configuration product dimension.</span></span> <span data-ttu-id="9ff7d-171">Hægt að velja eftirfarandi hluta á síðunni **Nafnakerfi afurðar**.</span><span class="sxs-lookup"><span data-stu-id="9ff7d-171">You can select the following segments on the **Product nomenclature** page:</span></span>

-   <span data-ttu-id="9ff7d-172">Gildi númeraraðar</span><span class="sxs-lookup"><span data-stu-id="9ff7d-172">Number sequence value</span></span>
-   <span data-ttu-id="9ff7d-173">Textafasti</span><span class="sxs-lookup"><span data-stu-id="9ff7d-173">Text constant</span></span>
-   <span data-ttu-id="9ff7d-174">Afbrigðisflokksvara</span><span class="sxs-lookup"><span data-stu-id="9ff7d-174">Configuration group item</span></span>

<span data-ttu-id="9ff7d-175">Nafnakerfi skilgreiningar má skilgreina fyrir uppskrift (BOM).</span><span class="sxs-lookup"><span data-stu-id="9ff7d-175">You can define a configuration nomenclature for a bill of materials (BOM).</span></span>

### <a name="example"></a><span data-ttu-id="9ff7d-176">Dæmi</span><span class="sxs-lookup"><span data-stu-id="9ff7d-176">Example</span></span>

<span data-ttu-id="9ff7d-177">Uppskrift hefur fjórar uppskriftalínur sem er skipt í tvo skilgreiningarflokka:</span><span class="sxs-lookup"><span data-stu-id="9ff7d-177">A BOM has four BOM lines that are divided into two configuration groups:</span></span>

-   <span data-ttu-id="9ff7d-178">Uppskriftarlínu: M0007, Staðlaða Cabinet</span><span class="sxs-lookup"><span data-stu-id="9ff7d-178">BOM line: M0007, Standard cabinet</span></span>
    -   <span data-ttu-id="9ff7d-179">Afbrigðaflokkur: Cabinet</span><span class="sxs-lookup"><span data-stu-id="9ff7d-179">Configuration group: Cabinet</span></span>
-   <span data-ttu-id="9ff7d-180">Uppskriftarlínu: M0008, háklassa cabinet</span><span class="sxs-lookup"><span data-stu-id="9ff7d-180">BOM line: M0008, High end cabinet</span></span>
    -   <span data-ttu-id="9ff7d-181">Afbrigðaflokkur: Cabinet</span><span class="sxs-lookup"><span data-stu-id="9ff7d-181">Configuration group: Cabinet</span></span>
-   <span data-ttu-id="9ff7d-182">Uppskriftarlínu: M0021, klæði framgrills</span><span class="sxs-lookup"><span data-stu-id="9ff7d-182">BOM line: M0021, Front grill cloth</span></span>
    -   <span data-ttu-id="9ff7d-183">Skilgreiningaflokkur: framgrill</span><span class="sxs-lookup"><span data-stu-id="9ff7d-183">Configuration group: Front grill</span></span>
-   <span data-ttu-id="9ff7d-184">Uppskriftarlínu: M0022, framgrill stál</span><span class="sxs-lookup"><span data-stu-id="9ff7d-184">BOM line: M0022, Front grill metal</span></span>
    -   <span data-ttu-id="9ff7d-185">Skilgreiningaflokkur: framgrill</span><span class="sxs-lookup"><span data-stu-id="9ff7d-185">Configuration group: Front grill</span></span>

<span data-ttu-id="9ff7d-186">Stofnað er nafnakerfi skilgreiningar sem inniheldur eftirfarandi hluta:</span><span class="sxs-lookup"><span data-stu-id="9ff7d-186">You create a configuration nomenclature that has the following segments:</span></span>

1.  <span data-ttu-id="9ff7d-187">Afbrigðaflokkur: Cabinet</span><span class="sxs-lookup"><span data-stu-id="9ff7d-187">Configuration group: Cabinet</span></span>
2.  <span data-ttu-id="9ff7d-188">Textafasti: "&"</span><span class="sxs-lookup"><span data-stu-id="9ff7d-188">Text constant: "&"</span></span>
3.  <span data-ttu-id="9ff7d-189">Skilgreiningaflokkur: framgrill</span><span class="sxs-lookup"><span data-stu-id="9ff7d-189">Configuration group: Front grill</span></span>

<span data-ttu-id="9ff7d-190">Í þessu tilfelli er skilgreiningarkenni fyrirstaðlaðan skáp sem er með framhlið úr tauklæði M0007&M0021.</span><span class="sxs-lookup"><span data-stu-id="9ff7d-190">In this case, the configuration ID for a standard cabinet that has a cloth front grill will be M0007&M0021.</span></span>

## <a name="nomenclature-for-a-combination-of-product-variants-and-configurations"></a><span data-ttu-id="9ff7d-191">Nafnakerfi fyrir samsetningu afurðarafbrigða og skilgreininga</span><span class="sxs-lookup"><span data-stu-id="9ff7d-191">Nomenclature for a combination of product variants and configurations</span></span>
<span data-ttu-id="9ff7d-192">Þegar þú notar annaðhvort tæknina skorðumiðaðar eða víddarbyggðar skilgreiningar til að skilgreina afurðarafbrigði fyrir afurðarsniðmát, geta afurðarsniðmát fengið númer afurðarafbrigðis sem innihalda nafnakerfið úr vídd skilgreiningarinnar.</span><span class="sxs-lookup"><span data-stu-id="9ff7d-192">When you use either the constraint-based configuration technology or the dimension-based configuration technology to configure product variants for a product master, the product variant numbers of the product variants can include the nomenclature from the configuration dimension.</span></span> <span data-ttu-id="9ff7d-193">Fylgja skal þessum skrefum til að skilgreina afbrigði.</span><span class="sxs-lookup"><span data-stu-id="9ff7d-193">Follow these steps to configure variants.</span></span>

1.  <span data-ttu-id="9ff7d-194">Skilgreina á nafnakerfi afurðarafbrigðisnúmers sem er með skilgreiningarvídd á síðunni **nafnakerfi afurðar**.</span><span class="sxs-lookup"><span data-stu-id="9ff7d-194">On the **Product nomenclature** page, define a product variant number nomenclature that includes the configuration dimension.</span></span>
2.  <span data-ttu-id="9ff7d-195">Úthluta þessa nafnakerfi á afurðarvíddarflokk með skilgreiningarvídd.</span><span class="sxs-lookup"><span data-stu-id="9ff7d-195">Assign the nomenclature to a product dimension group that has the configuration dimension.</span></span>
3.  <span data-ttu-id="9ff7d-196">Skilgreina nafnakerfi skilgreiningar fyrir íhlutina eða uppskriftirnar sem verða notaðar til að skilgreina afurðarafbrigðin.</span><span class="sxs-lookup"><span data-stu-id="9ff7d-196">Define a configuration nomenclature for the components or BOMs that will be used to configure the product variants.</span></span>

<span data-ttu-id="9ff7d-197">Einnig er hægt að stofna nafnakerfi fyrir afurðarafbrigðisheitin.</span><span class="sxs-lookup"><span data-stu-id="9ff7d-197">You can also create nomenclatures for the product variant names.</span></span> <span data-ttu-id="9ff7d-198">Heiti afurðarafbrgiða er hægt að skilgreina þannig að þau innihaldi kenni eða heiti skilgreiningarinnar.</span><span class="sxs-lookup"><span data-stu-id="9ff7d-198">The product variant names can be configured to include the configuration ID or name.</span></span>

### <a name="example-for-constraint-based-configurations"></a><span data-ttu-id="9ff7d-199">Dæmi um skorðuskilgreiningar</span><span class="sxs-lookup"><span data-stu-id="9ff7d-199">Example for constraint-based configurations</span></span>

<span data-ttu-id="9ff7d-200">Í þessu dæmi er notað nafnakerfi afurðarafbrigðisnúmers sem samanstendur úr eftirfarandi hlutum:</span><span class="sxs-lookup"><span data-stu-id="9ff7d-200">For this example, you use a product variant number nomenclature that consists of the following segments:</span></span>

1.  <span data-ttu-id="9ff7d-201">Númer afurðarsniðmáts</span><span class="sxs-lookup"><span data-stu-id="9ff7d-201">Product master number</span></span>
2.  <span data-ttu-id="9ff7d-202">Textafasti "\_"</span><span class="sxs-lookup"><span data-stu-id="9ff7d-202">Text constant "\_"</span></span>
3.  <span data-ttu-id="9ff7d-203">Afbrigði</span><span class="sxs-lookup"><span data-stu-id="9ff7d-203">Configuration</span></span>

<span data-ttu-id="9ff7d-204">Nafnakerfi skilgreiningar inniheldur eftirfarandi hluta:</span><span class="sxs-lookup"><span data-stu-id="9ff7d-204">The configuration nomenclature consists of the following segments:</span></span>

1.  <span data-ttu-id="9ff7d-205">Eigindargildi: Efni</span><span class="sxs-lookup"><span data-stu-id="9ff7d-205">Attribute value: Material</span></span>
2.  <span data-ttu-id="9ff7d-206">Textafasti: "AAA"</span><span class="sxs-lookup"><span data-stu-id="9ff7d-206">Text constant: "AAA"</span></span>
3.  <span data-ttu-id="9ff7d-207">Eigindargildi: Lengd</span><span class="sxs-lookup"><span data-stu-id="9ff7d-207">Attribute value: Length</span></span>

<span data-ttu-id="9ff7d-208">Hægt er að færa inn eftirfarandi gildi fyrir hluta:</span><span class="sxs-lookup"><span data-stu-id="9ff7d-208">You enter the following values for segments:</span></span>

-   <span data-ttu-id="9ff7d-209">Númer afurðarsniðmáts = **M0099**</span><span class="sxs-lookup"><span data-stu-id="9ff7d-209">Product master number = **M0099**</span></span>
-   <span data-ttu-id="9ff7d-210">Efni = **Plast**</span><span class="sxs-lookup"><span data-stu-id="9ff7d-210">Material = **Plastic**</span></span>
-   <span data-ttu-id="9ff7d-211">Lengd = **12**</span><span class="sxs-lookup"><span data-stu-id="9ff7d-211">Length = **12**</span></span>

<span data-ttu-id="9ff7d-212">Í þessu tilviki verður afurðarafbrigðisnúmerið M0099\_PlasticAAA12.</span><span class="sxs-lookup"><span data-stu-id="9ff7d-212">In this case, the product variant number will be M0099\_PlasticAAA12.</span></span>

### <a name="example-for-dimension-based-configurations"></a><span data-ttu-id="9ff7d-213">Dæmi um víddarbyggðar skilgreiningar</span><span class="sxs-lookup"><span data-stu-id="9ff7d-213">Example for dimension-based configurations</span></span>

<span data-ttu-id="9ff7d-214">Í þessu dæmi er notað nafnakerfi afurðarafbrigðisnúmers sem samanstendur úr eftirfarandi hlutum:</span><span class="sxs-lookup"><span data-stu-id="9ff7d-214">For this example, you use a product variant number nomenclature that consists of the following segments:</span></span>

1.  <span data-ttu-id="9ff7d-215">Númer afurðarsniðmáts</span><span class="sxs-lookup"><span data-stu-id="9ff7d-215">Product master number</span></span>
2.  <span data-ttu-id="9ff7d-216">Textafasti "//"</span><span class="sxs-lookup"><span data-stu-id="9ff7d-216">Text constant "//"</span></span>
3.  <span data-ttu-id="9ff7d-217">Afbrigði</span><span class="sxs-lookup"><span data-stu-id="9ff7d-217">Configuration</span></span>

<span data-ttu-id="9ff7d-218">Nafnakerfi skilgreiningar inniheldur eftirfarandi hluta:</span><span class="sxs-lookup"><span data-stu-id="9ff7d-218">The configuration nomenclature consists of the following segments:</span></span>

1.  <span data-ttu-id="9ff7d-219">Afbrigðaflokkur: Cabinet</span><span class="sxs-lookup"><span data-stu-id="9ff7d-219">Configuration group: Cabinet</span></span>
2.  <span data-ttu-id="9ff7d-220">Textafasti: "&"</span><span class="sxs-lookup"><span data-stu-id="9ff7d-220">Text constant: "&"</span></span>
3.  <span data-ttu-id="9ff7d-221">Skilgreiningaflokkur: framgrill</span><span class="sxs-lookup"><span data-stu-id="9ff7d-221">Configuration group: Front grill</span></span>

<span data-ttu-id="9ff7d-222">Hægt er að færa inn eftirfarandi gildi fyrir hluta:</span><span class="sxs-lookup"><span data-stu-id="9ff7d-222">You enter the following values for segments:</span></span>

-   <span data-ttu-id="9ff7d-223">Númer afurðarsniðmáts = **D0123**</span><span class="sxs-lookup"><span data-stu-id="9ff7d-223">Product master number = **D0123**</span></span>
-   <span data-ttu-id="9ff7d-224">Skápur = **M0008**</span><span class="sxs-lookup"><span data-stu-id="9ff7d-224">Cabinet = **M0008**</span></span>
-   <span data-ttu-id="9ff7d-225">Framhlið = **M0022**</span><span class="sxs-lookup"><span data-stu-id="9ff7d-225">Front grill = **M0022**</span></span>

<span data-ttu-id="9ff7d-226">Í þessu tilviki verður afurðarafbrigðisnúmerið D0123//M0008&M0022.</span><span class="sxs-lookup"><span data-stu-id="9ff7d-226">In this case, the product variant number will be D0123//M0008&M0022.</span></span>

## <a name="numbering-conflicts"></a><span data-ttu-id="9ff7d-227">Árekstrar númera</span><span class="sxs-lookup"><span data-stu-id="9ff7d-227">Numbering conflicts</span></span>
<span data-ttu-id="9ff7d-228">Mögulegt er að setja upp afurð nafnakerfi afurðarafbrigðisnúmers sem leiðir ekki til einkvæmra númera afurðarafbrigða.</span><span class="sxs-lookup"><span data-stu-id="9ff7d-228">In some cases, a product variant number nomenclature that you set up might not produce unique product variant numbers.</span></span> <span data-ttu-id="9ff7d-229">Til dæmis verða númer afurðarafbrigða ekki einnkvæm ef ein virk afurðarvídd er ekki innifalin í nafnakerfi fyrir afurðarsniðmát sem notar forskilgreinda tækni til skilgreiningar afbrigða.</span><span class="sxs-lookup"><span data-stu-id="9ff7d-229">For example, the product variant numbers won't be unique if one active product dimension isn't included in the nomenclature for a product master that uses the predefined variant configuration technology.</span></span> <span data-ttu-id="9ff7d-230">Aðferðin til að meðhöndla árekstra er breytileg eftir tækni við skilgreiningu.</span><span class="sxs-lookup"><span data-stu-id="9ff7d-230">The way that you handle conflicts varies, depending on the configuration technology.</span></span>

### <a name="predefined-variants"></a><span data-ttu-id="9ff7d-231">Forskilgreint afbrigði</span><span class="sxs-lookup"><span data-stu-id="9ff7d-231">Predefined variants</span></span>

<span data-ttu-id="9ff7d-232">Villa mun eiga sér stað ef reynt er að handvirkt eða sjálfkrafa mynda afurðarafbrigði þar sem eitt eða fleiri afurðarafbrigði endar á því að hafa sama númer afurðarafbrigðis.</span><span class="sxs-lookup"><span data-stu-id="9ff7d-232">An error occurs if you try to manually create or automatically generate product variants, and more than one product variant ends up with the same product variant number.</span></span> <span data-ttu-id="9ff7d-233">Til að forðast slíkt ætti frekar að nota allar virkar afurðarvíddar í afurðavíddaflokki.</span><span class="sxs-lookup"><span data-stu-id="9ff7d-233">To avoid this scenario, you should use all active product dimensions in the product dimension group.</span></span> <span data-ttu-id="9ff7d-234">Einnig er hægt að hafa með númeraröð til að tryggja enn betur að afurðarafbrigðisnúmerin séu einkvæm.</span><span class="sxs-lookup"><span data-stu-id="9ff7d-234">Alternatively, include a number sequence to help guarantee that the product variant numbers are unique.</span></span>

### <a name="constraint-based-configurations"></a><span data-ttu-id="9ff7d-235">Skorðuskilgreiningar</span><span class="sxs-lookup"><span data-stu-id="9ff7d-235">Constraint-based configurations</span></span>

<span data-ttu-id="9ff7d-236">Allt eftir nafnakerfinu getur kerfið reynt að úthluta númeri afurðarafbrigðis sem ekki er einkvæmt á skilgreiningu.</span><span class="sxs-lookup"><span data-stu-id="9ff7d-236">Depending on the nomenclature, the system might try to assign a non-unique product variant number to a configuration.</span></span> <span data-ttu-id="9ff7d-237">Í slíku tilfelli mun kerfið nota númeraröð fyrir vídd skilgreiningarvíddina sem númer afurðarafbrigðis í staðinn. Ef það gerist, mun viðvörun berast.</span><span class="sxs-lookup"><span data-stu-id="9ff7d-237">In this case, the system uses the number sequence for the configuration dimension as the product variant number instead, and you receive a warning.</span></span> <span data-ttu-id="9ff7d-238">Til að forðast slíkt ætti að taka með nógu margar eigindir í nafnakerfið til að stuðla að því að tryggja einkvæm afurðarafbrigðanúmer.</span><span class="sxs-lookup"><span data-stu-id="9ff7d-238">To avoid this scenario, you should include enough attributes in the nomenclature to help guarantee unique product variant numbers.</span></span> <span data-ttu-id="9ff7d-239">Einnig ætti að ganga úr skugga um að kveikt sé á valkostinum **Endurnota** fyrir íhlutinn.</span><span class="sxs-lookup"><span data-stu-id="9ff7d-239">You should also make sure that the **Reuse** option is turned on for the component.</span></span>

### <a name="dimension-based-configurations"></a><span data-ttu-id="9ff7d-240">Víddaskilgreiningar</span><span class="sxs-lookup"><span data-stu-id="9ff7d-240">Dimension-based configurations</span></span>

<span data-ttu-id="9ff7d-241">Á einu þrefi skilgreiningarferlisins leggur kerfið til skilgreiningargildi í samræmi við nafnakerfið.</span><span class="sxs-lookup"><span data-stu-id="9ff7d-241">During one step of the configuration process, the system suggests a configuration value according to the nomenclature.</span></span> <span data-ttu-id="9ff7d-242">Í þessu skrefi geturðu Handvirkt breytt gildi skilgreiningarinnar.</span><span class="sxs-lookup"><span data-stu-id="9ff7d-242">In this step, you can manually change the configuration value.</span></span> <span data-ttu-id="9ff7d-243">Þegar skilgreining er vistuð, mun kerfið athuga hvort gildi skilgreiningar er einkvæmt.</span><span class="sxs-lookup"><span data-stu-id="9ff7d-243">When you save the configuration, the system verifies that the configuration value is unique.</span></span> <span data-ttu-id="9ff7d-244">Ef gildið sem fært er inn er ekki einkvæmt verða send villuboð.</span><span class="sxs-lookup"><span data-stu-id="9ff7d-244">If the value that you entered isn't unique, you receive an error message.</span></span> <span data-ttu-id="9ff7d-245">Færa þarf inn gildi einkvæmrar skilgreiningar til að vista skilgreininguna.</span><span class="sxs-lookup"><span data-stu-id="9ff7d-245">To save the configuration, you must enter a unique configuration value.</span></span>

<a name="see-also"></a><span data-ttu-id="9ff7d-246">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="9ff7d-246">See also</span></span>
--------

[<span data-ttu-id="9ff7d-247">Stofna nafnakerfi afurðarnúmers fyrir fyrirframskilgreind afurðarafbrigði</span><span class="sxs-lookup"><span data-stu-id="9ff7d-247">Create a product number nomenclature for predefined product variants</span></span>](/dynamics365/unified-operations/supply-chain/pim/tasks/create-product-number-nomenclature-predefined-variants-2016-11)

[<span data-ttu-id="9ff7d-248">Stofna nafnakerfi afurðarafbrigðis fyrir skilgreind afurðarafbrigði</span><span class="sxs-lookup"><span data-stu-id="9ff7d-248">Create a product number nomenclature for configured product variants</span></span>](/dynamics365/unified-operations/supply-chain/pim/tasks/create-product-number-nomenclature-product-variants_2016_11)


