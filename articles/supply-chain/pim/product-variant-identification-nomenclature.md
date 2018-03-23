---
title: "Nafnakerfi afurðarafbrigðisnúmera og -nafna"
description: "Þetta efnisatriði lýsir því hvernig hægt er að setja upp nafnakerfi afurðarnúmers til að skipta út föstu sniði [Númer afurðarsniðmáts - Skilgreining - Stærð - Litur - Stíll]."
author: roxanadiaconu
manager: AnnBe
ms.date: 11/03/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: EcoResNomenclature, EcoResProductDimensionGroup, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelDetails
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 220104
ms.assetid: 3fe69fb7-5c32-423c-98a8-2f53186cda68
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: HT
ms.sourcegitcommit: 72d4ff5e1311005d3bf43a13e28208cd9b3d1457
ms.openlocfilehash: 6a620f2a0105d578d419d3aac816c7d78fbf3e46
ms.contentlocale: is-is
ms.lasthandoff: 03/08/2018

---

# <a name="nomenclature-of-product-variant-numbers-and-names"></a><span data-ttu-id="f0cdb-103">Nafnakerfi afurðarafbrigðisnúmera og -nafna</span><span class="sxs-lookup"><span data-stu-id="f0cdb-103">Nomenclature of product variant numbers and names</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="f0cdb-104">Þetta efnisatriði lýsir því hvernig hægt er að setja upp nafnakerfi afurðarnúmers til að skipta út föstu sniði [Númer afurðarsniðmáts - Skilgreining - Stærð - Litur - Stíll].</span><span class="sxs-lookup"><span data-stu-id="f0cdb-104">This topic describes how you can set up a product number nomenclature to replace the fixed [Product master number - Configuration - Size - Color - Style] format.</span></span> <span data-ttu-id="f0cdb-105">Nýja nafnakerfið er með markað snið sem tekur til númers afurðarsniðmátsins, virku afurðavíddanna og skiltákna texta að eigin vali.</span><span class="sxs-lookup"><span data-stu-id="f0cdb-105">The new nomenclature has a targeted format that includes the product master number, active product dimensions, and text delimiters of your choice.</span></span> <span data-ttu-id="f0cdb-106">Einnig er hægt að stofna nafnakerfi fyrir afurðaheiti.</span><span class="sxs-lookup"><span data-stu-id="f0cdb-106">You can also create a nomenclature for product names.</span></span> <span data-ttu-id="f0cdb-107">Loks er hægt að búa til nafnakerfi til að auðkenna grunnstillingar sem eru stofnaðar af skorðumiðuðum afurðarafbrigðastilli.</span><span class="sxs-lookup"><span data-stu-id="f0cdb-107">Finally, you can build a nomenclature to identify configurations that are created by the constraint-based product configurator.</span></span> <span data-ttu-id="f0cdb-108">Þessum nafnakerfi geta innihaldið eigindir að eigin vali.</span><span class="sxs-lookup"><span data-stu-id="f0cdb-108">These nomenclatures can contain attributes of your choice.</span></span>

<span data-ttu-id="f0cdb-109">Ný nafnakerfi fyrir afurðarafbrigðanúmer og afurðarafbrigðaheiti gera þér kleift að taka með hluta auðkennanna fyrir afurðarafbrigði.</span><span class="sxs-lookup"><span data-stu-id="f0cdb-109">The new nomenclatures for product variant numbers and product variant names let you include segments in the identifiers for product variants.</span></span> <span data-ttu-id="f0cdb-110">Slíkir hluta geta falið í sér afurðarsniðmát, númer og heiti, auðkenni afurðavídda og heiti, númeraraðir, textafasta og eigindir.</span><span class="sxs-lookup"><span data-stu-id="f0cdb-110">These segments can include the product master number and name, product dimension IDs and names, number sequences, text constants, and attributes.</span></span> <span data-ttu-id="f0cdb-111">Þessi virkni leyfir þér að finna á fljótan hátt tilteknar afurðarafbrigði þegar þú stofnar sölupöntun eða innkaupapöntun.</span><span class="sxs-lookup"><span data-stu-id="f0cdb-111">This functionality lets you quickly find a specific product variant when you create a sales order or a purchase order.</span></span> <span data-ttu-id="f0cdb-112">Nafnakerfi fyrir bæði afurðarafbrigðanúmer og afurðarafbrigðaheiti eru stofnuð með því að nota síðuna **Nafnakerfi afurðar**.</span><span class="sxs-lookup"><span data-stu-id="f0cdb-112">You create nomenclatures for both product variant numbers and product variant names by using the **Product nomenclature** page.</span></span> <span data-ttu-id="f0cdb-113">Til að opna þessa síðu er smellt á **afurðaupplýsingastjórnun,** &gt; **Uppsetning**.</span><span class="sxs-lookup"><span data-stu-id="f0cdb-113">To open this page, click **Product information management** &gt; **Setup**.</span></span>

## <a name="nomenclature-of-predefined-product-variants"></a><span data-ttu-id="f0cdb-114">Nafnakerfi fyrirframskilgreindra afurðarafbrigða</span><span class="sxs-lookup"><span data-stu-id="f0cdb-114">Nomenclature of predefined product variants</span></span>
<span data-ttu-id="f0cdb-115">Afurðarafbrigði eru myndaðar fyrir afurðarsniðmát í samræmi við eina af þremur afbrigðistækni:</span><span class="sxs-lookup"><span data-stu-id="f0cdb-115">Product variants are generated for product masters according to one of three configuration technologies:</span></span>

-   <span data-ttu-id="f0cdb-116">Forskilgreint afbrigði</span><span class="sxs-lookup"><span data-stu-id="f0cdb-116">Predefined variants</span></span>
-   <span data-ttu-id="f0cdb-117">Skorðumiðað</span><span class="sxs-lookup"><span data-stu-id="f0cdb-117">Constraint-based</span></span>
-   <span data-ttu-id="f0cdb-118">Víddarmiðað</span><span class="sxs-lookup"><span data-stu-id="f0cdb-118">Dimension-based</span></span>

<span data-ttu-id="f0cdb-119">Hvert afurðarafbrigði hefur númer og heiti og nafnakerfi auðkennins afurðarafbrigðis leyfir þér að velja hlutana sem verða hafðir með í hverju númeri eða heiti afurðarafbrigðis.</span><span class="sxs-lookup"><span data-stu-id="f0cdb-119">Each product variant has a number and a name, and the product variant identification nomenclatures let you select the segments that will be included in each product variant number or name.</span></span> <span data-ttu-id="f0cdb-120">Hægt að velja eftirfarandi hluta á síðunni **Nafnakerfi afurðar**.</span><span class="sxs-lookup"><span data-stu-id="f0cdb-120">You can select the following segments on the **Product nomenclature** page:</span></span>

-   <span data-ttu-id="f0cdb-121">Númer afurðarsniðmáts</span><span class="sxs-lookup"><span data-stu-id="f0cdb-121">Product master number</span></span>
-   <span data-ttu-id="f0cdb-122">Heiti afurðarsniðmáts</span><span class="sxs-lookup"><span data-stu-id="f0cdb-122">Product master name</span></span>
-   <span data-ttu-id="f0cdb-123">Gildi númeraraðar</span><span class="sxs-lookup"><span data-stu-id="f0cdb-123">Number sequence value</span></span>
-   <span data-ttu-id="f0cdb-124">Textafasti</span><span class="sxs-lookup"><span data-stu-id="f0cdb-124">Text constant</span></span>
-   <span data-ttu-id="f0cdb-125">Afurðarvíddir</span><span class="sxs-lookup"><span data-stu-id="f0cdb-125">Product dimensions</span></span>
    -   <span data-ttu-id="f0cdb-126">Veljið skilgreiningarkenni eða -heiti</span><span class="sxs-lookup"><span data-stu-id="f0cdb-126">Configuration ID or name</span></span>
    -   <span data-ttu-id="f0cdb-127">Kenni eða heiti litar</span><span class="sxs-lookup"><span data-stu-id="f0cdb-127">Color ID or name</span></span>
    -   <span data-ttu-id="f0cdb-128">Kenni eða heiti stærðar</span><span class="sxs-lookup"><span data-stu-id="f0cdb-128">Size ID or name</span></span>
    -   <span data-ttu-id="f0cdb-129">Kenni eða heiti stílsniðs</span><span class="sxs-lookup"><span data-stu-id="f0cdb-129">Style ID or name</span></span>

<span data-ttu-id="f0cdb-130">Eftir að auðkenni nafnakerfis afurðarafbrigðis er skilgreint, er hægt að tengja það við afurðarvíddarflokk.</span><span class="sxs-lookup"><span data-stu-id="f0cdb-130">After you define a product variant identification number nomenclature, you can associate it with a product dimension group.</span></span> <span data-ttu-id="f0cdb-131">Þá verður öllum afurðarsniðmátum sem vísa til þessa afurðarvíddarflokks úthlutað númerum afurðarafbrigða í samræmi við nafnakerfið.</span><span class="sxs-lookup"><span data-stu-id="f0cdb-131">All product masters that reference this product dimension group will then be assigned product variant numbers according to the nomenclature.</span></span> <span data-ttu-id="f0cdb-132">Nafnakerfi fyrir afurðaafbrigðaheiti er hins vegar ekki hægt að tengja við afurðavíddaflokka.</span><span class="sxs-lookup"><span data-stu-id="f0cdb-132">However, product variant name nomenclatures can't be associated with product dimension groups.</span></span> <span data-ttu-id="f0cdb-133">Einnig má tengja nafnakerfi fyrir auðkenni afurðarafbrigðis beint við aðalsniðmát.</span><span class="sxs-lookup"><span data-stu-id="f0cdb-133">You can also assign a product variant identification nomenclature directly to a product master.</span></span> <span data-ttu-id="f0cdb-134">Í því rtilviki verður afurðarafbrigðim sem tilheyra afurðasniðmátinu úthlutað afurðarafbrigðanúmerum og -heitum í samræmi við nafnakerfin.</span><span class="sxs-lookup"><span data-stu-id="f0cdb-134">In this case, the product variants that belong to the product master will be assigned product variant numbers and names according to the nomenclatures.</span></span>

### <a name="example"></a><span data-ttu-id="f0cdb-135">Dæmi</span><span class="sxs-lookup"><span data-stu-id="f0cdb-135">Example</span></span>

<span data-ttu-id="f0cdb-136">Stuttermabolur (TS1234) er framleiddur í þremur stærðum (S, M, L) fjórum litum (Rauður, Grænn, Blár, Gulur) og tveimur sniðum (pólóbolur, vaffhálsmál).</span><span class="sxs-lookup"><span data-stu-id="f0cdb-136">A T-shirt (TS1234) is produced in three sizes (S, M, L), four colors (Red, Green, Blue, Yellow), and two styles (Polo, V).</span></span> <span data-ttu-id="f0cdb-137">Þar af leiðir að 24 afurðarafbrigði eru möguleg (= 3 × 4 × 2).</span><span class="sxs-lookup"><span data-stu-id="f0cdb-137">Therefore, 24 product variants are possible (= 3 × 4 × 2).</span></span> <span data-ttu-id="f0cdb-138">Stofnað er nafnakerfi fyrir afurðarafbrigðisnúmer sem hefur eftirfarandi hluta:</span><span class="sxs-lookup"><span data-stu-id="f0cdb-138">You create a product variant number nomenclature that has the following segments:</span></span>

1.  <span data-ttu-id="f0cdb-139">Númer afurðarsniðmáts</span><span class="sxs-lookup"><span data-stu-id="f0cdb-139">Product master number</span></span>
2.  <span data-ttu-id="f0cdb-140">Textafasti: "-"</span><span class="sxs-lookup"><span data-stu-id="f0cdb-140">Text constant: "-"</span></span>
3.  <span data-ttu-id="f0cdb-141">Litur</span><span class="sxs-lookup"><span data-stu-id="f0cdb-141">Color</span></span>
4.  <span data-ttu-id="f0cdb-142">Textafasti: "-"</span><span class="sxs-lookup"><span data-stu-id="f0cdb-142">Text constant: "-"</span></span>
5.  <span data-ttu-id="f0cdb-143">Stærð</span><span class="sxs-lookup"><span data-stu-id="f0cdb-143">Size</span></span>
6.  <span data-ttu-id="f0cdb-144">Textafasti: "-"</span><span class="sxs-lookup"><span data-stu-id="f0cdb-144">Text constant: "-"</span></span>
7.  <span data-ttu-id="f0cdb-145">Stíll</span><span class="sxs-lookup"><span data-stu-id="f0cdb-145">Style</span></span>

<span data-ttu-id="f0cdb-146">Í þessu tilviki er afurðarafbrigðisnúmer fyrir rauðan, lítill pólóbol fyrir TS1234-Red-Small-Polo.</span><span class="sxs-lookup"><span data-stu-id="f0cdb-146">In this case, the product variant number for a red, small, polo T-shirt will be TS1234-Red-Small-Polo.</span></span>

## <a name="nomenclature-of-constraint-based-configurations"></a><span data-ttu-id="f0cdb-147">Nafnakerfi skorðuskilgreininga</span><span class="sxs-lookup"><span data-stu-id="f0cdb-147">Nomenclature of constraint-based configurations</span></span>
<span data-ttu-id="f0cdb-148">Fyrir skorðuskilgreiningar er hægt að stofna sérhæft nafnakerfi fyrir skilgreiningu afurðarvídda.</span><span class="sxs-lookup"><span data-stu-id="f0cdb-148">For constraint-based configurations, you can create a dedicated nomenclature for the configuration product dimension.</span></span> <span data-ttu-id="f0cdb-149">Hægt að velja eftirfarandi hluta á síðunni **Nafnakerfi afurðar**.</span><span class="sxs-lookup"><span data-stu-id="f0cdb-149">You can select the following segments on the **Product nomenclature** page:</span></span>

-   <span data-ttu-id="f0cdb-150">Gildi númeraraðar</span><span class="sxs-lookup"><span data-stu-id="f0cdb-150">Number sequence value</span></span>
-   <span data-ttu-id="f0cdb-151">Textafasti</span><span class="sxs-lookup"><span data-stu-id="f0cdb-151">Text constant</span></span>
-   <span data-ttu-id="f0cdb-152">Eigindargildi</span><span class="sxs-lookup"><span data-stu-id="f0cdb-152">Attribute value</span></span>

<span data-ttu-id="f0cdb-153">Hver þáttur í afbrigðalíkan afurðar getur haft sitt eigið skilgreinda nafnakerfi.</span><span class="sxs-lookup"><span data-stu-id="f0cdb-153">Each component in a product configuration model can have its own configuration nomenclature.</span></span> <span data-ttu-id="f0cdb-154">Aðeins má nota eigindir sem tilheyra íhlutnum.</span><span class="sxs-lookup"><span data-stu-id="f0cdb-154">Only attributes that belong to the component can be used.</span></span> <span data-ttu-id="f0cdb-155">Eigindir úr undiríhlutir eða notendakröfur eru ekki nothæfar.</span><span class="sxs-lookup"><span data-stu-id="f0cdb-155">Attributes from subcomponents or user requirements can't be used.</span></span>

### <a name="example"></a><span data-ttu-id="f0cdb-156">Dæmi</span><span class="sxs-lookup"><span data-stu-id="f0cdb-156">Example</span></span>

<span data-ttu-id="f0cdb-157">Afbrigðalíkan afurðar hefur rótaríhlut með tvær eigindir:</span><span class="sxs-lookup"><span data-stu-id="f0cdb-157">A product configuration model has a root component that has two attributes:</span></span>

-   <span data-ttu-id="f0cdb-158">Efni (Plast, viður, Stáli)</span><span class="sxs-lookup"><span data-stu-id="f0cdb-158">Material (Plastic, Wood, Steel)</span></span>
-   <span data-ttu-id="f0cdb-159">Lengd (10... 100)</span><span class="sxs-lookup"><span data-stu-id="f0cdb-159">Length (10...100)</span></span>

<span data-ttu-id="f0cdb-160">Stofnað er nafnakerfi skilgreiningar sem inniheldur eftirfarandi hluta:</span><span class="sxs-lookup"><span data-stu-id="f0cdb-160">You create a configuration nomenclature that has the following segments:</span></span>

1.  <span data-ttu-id="f0cdb-161">Eigindargildi: Efni</span><span class="sxs-lookup"><span data-stu-id="f0cdb-161">Attribute value: Material</span></span>
2.  <span data-ttu-id="f0cdb-162">Textafasti: "AAA"</span><span class="sxs-lookup"><span data-stu-id="f0cdb-162">Text constant: "AAA"</span></span>
3.  <span data-ttu-id="f0cdb-163">Eigindargildi: Lengd</span><span class="sxs-lookup"><span data-stu-id="f0cdb-163">Attribute value: Length</span></span>

<span data-ttu-id="f0cdb-164">Í þessu tilfelli er skilgreiningarkenni fyrir viðarefni sem er 78 á lengd WoodAAA78.</span><span class="sxs-lookup"><span data-stu-id="f0cdb-164">In this case, the configuration ID for wood material that has a length of 78 will be WoodAAA78.</span></span>

## <a name="nomenclature-of-dimension-based-configurations"></a><span data-ttu-id="f0cdb-165">Víddarbyggðrar skilgreiningar Nafnakerfis</span><span class="sxs-lookup"><span data-stu-id="f0cdb-165">Nomenclature of dimension-based configurations</span></span>
<span data-ttu-id="f0cdb-166">Fyrir skorðuskilgreiningar er hægt að stofna sérhæft nafnakerfi fyrir skilgreiningu afurðarvídda.</span><span class="sxs-lookup"><span data-stu-id="f0cdb-166">For dimension-based configurations, you can create a dedicated nomenclature for the configuration product dimension.</span></span> <span data-ttu-id="f0cdb-167">Hægt að velja eftirfarandi hluta á síðunni **Nafnakerfi afurðar**.</span><span class="sxs-lookup"><span data-stu-id="f0cdb-167">You can select the following segments on the **Product nomenclature** page:</span></span>

-   <span data-ttu-id="f0cdb-168">Gildi númeraraðar</span><span class="sxs-lookup"><span data-stu-id="f0cdb-168">Number sequence value</span></span>
-   <span data-ttu-id="f0cdb-169">Textafasti</span><span class="sxs-lookup"><span data-stu-id="f0cdb-169">Text constant</span></span>
-   <span data-ttu-id="f0cdb-170">Afbrigðisflokksvara</span><span class="sxs-lookup"><span data-stu-id="f0cdb-170">Configuration group item</span></span>

<span data-ttu-id="f0cdb-171">Nafnakerfi skilgreiningar má skilgreina fyrir uppskrift (BOM).</span><span class="sxs-lookup"><span data-stu-id="f0cdb-171">You can define a configuration nomenclature for a bill of materials (BOM).</span></span>

### <a name="example"></a><span data-ttu-id="f0cdb-172">Dæmi</span><span class="sxs-lookup"><span data-stu-id="f0cdb-172">Example</span></span>

<span data-ttu-id="f0cdb-173">Uppskrift hefur fjórar uppskriftalínur sem er skipt í tvo skilgreiningarflokka:</span><span class="sxs-lookup"><span data-stu-id="f0cdb-173">A BOM has four BOM lines that are divided into two configuration groups:</span></span>

-   <span data-ttu-id="f0cdb-174">Uppskriftarlínu: M0007, Staðlaða Cabinet</span><span class="sxs-lookup"><span data-stu-id="f0cdb-174">BOM line: M0007, Standard cabinet</span></span>
    -   <span data-ttu-id="f0cdb-175">Afbrigðaflokkur: Cabinet</span><span class="sxs-lookup"><span data-stu-id="f0cdb-175">Configuration group: Cabinet</span></span>
-   <span data-ttu-id="f0cdb-176">Uppskriftarlínu: M0008, háklassa cabinet</span><span class="sxs-lookup"><span data-stu-id="f0cdb-176">BOM line: M0008, High end cabinet</span></span>
    -   <span data-ttu-id="f0cdb-177">Afbrigðaflokkur: Cabinet</span><span class="sxs-lookup"><span data-stu-id="f0cdb-177">Configuration group: Cabinet</span></span>
-   <span data-ttu-id="f0cdb-178">Uppskriftarlínu: M0021, klæði framgrills</span><span class="sxs-lookup"><span data-stu-id="f0cdb-178">BOM line: M0021, Front grill cloth</span></span>
    -   <span data-ttu-id="f0cdb-179">Skilgreiningaflokkur: framgrill</span><span class="sxs-lookup"><span data-stu-id="f0cdb-179">Configuration group: Front grill</span></span>
-   <span data-ttu-id="f0cdb-180">Uppskriftarlínu: M0022, framgrill stál</span><span class="sxs-lookup"><span data-stu-id="f0cdb-180">BOM line: M0022, Front grill metal</span></span>
    -   <span data-ttu-id="f0cdb-181">Skilgreiningaflokkur: framgrill</span><span class="sxs-lookup"><span data-stu-id="f0cdb-181">Configuration group: Front grill</span></span>

<span data-ttu-id="f0cdb-182">Stofnað er nafnakerfi skilgreiningar sem inniheldur eftirfarandi hluta:</span><span class="sxs-lookup"><span data-stu-id="f0cdb-182">You create a configuration nomenclature that has the following segments:</span></span>

1.  <span data-ttu-id="f0cdb-183">Afbrigðaflokkur: Cabinet</span><span class="sxs-lookup"><span data-stu-id="f0cdb-183">Configuration group: Cabinet</span></span>
2.  <span data-ttu-id="f0cdb-184">Textafasti: "&"</span><span class="sxs-lookup"><span data-stu-id="f0cdb-184">Text constant: "&"</span></span>
3.  <span data-ttu-id="f0cdb-185">Skilgreiningaflokkur: framgrill</span><span class="sxs-lookup"><span data-stu-id="f0cdb-185">Configuration group: Front grill</span></span>

<span data-ttu-id="f0cdb-186">Í þessu tilfelli er skilgreiningarkenni fyrirstaðlaðan skáp sem er með framhlið úr tauklæði M0007&M0021.</span><span class="sxs-lookup"><span data-stu-id="f0cdb-186">In this case, the configuration ID for a standard cabinet that has a cloth front grill will be M0007&M0021.</span></span>

## <a name="nomenclature-for-a-combination-of-product-variants-and-configurations"></a><span data-ttu-id="f0cdb-187">Nafnakerfi fyrir samsetningu afurðarafbrigða og skilgreininga</span><span class="sxs-lookup"><span data-stu-id="f0cdb-187">Nomenclature for a combination of product variants and configurations</span></span>
<span data-ttu-id="f0cdb-188">Þegar þú notar annaðhvort tæknina skorðumiðaðar eða víddarbyggðar skilgreiningar til að skilgreina afurðarafbrigði fyrir afurðarsniðmát, geta afurðarsniðmát fengið númer afurðarafbrigðis sem innihalda nafnakerfið úr vídd skilgreiningarinnar.</span><span class="sxs-lookup"><span data-stu-id="f0cdb-188">When you use either the constraint-based configuration technology or the dimension-based configuration technology to configure product variants for a product master, the product variant numbers of the product variants can include the nomenclature from the configuration dimension.</span></span> <span data-ttu-id="f0cdb-189">Fylgja skal þessum skrefum til að skilgreina afbrigði.</span><span class="sxs-lookup"><span data-stu-id="f0cdb-189">Follow these steps to configure variants.</span></span>

1.  <span data-ttu-id="f0cdb-190">Skilgreina á nafnakerfi afurðarafbrigðisnúmers sem er með skilgreiningarvídd á síðunni **nafnakerfi afurðar**.</span><span class="sxs-lookup"><span data-stu-id="f0cdb-190">On the **Product nomenclature** page, define a product variant number nomenclature that includes the configuration dimension.</span></span>
2.  <span data-ttu-id="f0cdb-191">Úthluta þessa nafnakerfi á afurðarvíddarflokk með skilgreiningarvídd.</span><span class="sxs-lookup"><span data-stu-id="f0cdb-191">Assign the nomenclature to a product dimension group that has the configuration dimension.</span></span>
3.  <span data-ttu-id="f0cdb-192">Skilgreina nafnakerfi skilgreiningar fyrir íhlutina eða uppskriftirnar sem verða notaðar til að skilgreina afurðarafbrigðin.</span><span class="sxs-lookup"><span data-stu-id="f0cdb-192">Define a configuration nomenclature for the components or BOMs that will be used to configure the product variants.</span></span>

<span data-ttu-id="f0cdb-193">Einnig er hægt að stofna nafnakerfi fyrir afurðarafbrigðisheitin.</span><span class="sxs-lookup"><span data-stu-id="f0cdb-193">You can also create nomenclatures for the product variant names.</span></span> <span data-ttu-id="f0cdb-194">Heiti afurðarafbrgiða er hægt að skilgreina þannig að þau innihaldi kenni eða heiti skilgreiningarinnar.</span><span class="sxs-lookup"><span data-stu-id="f0cdb-194">The product variant names can be configured to include the configuration ID or name.</span></span>

### <a name="example-for-constraint-based-configurations"></a><span data-ttu-id="f0cdb-195">Dæmi um skorðuskilgreiningar</span><span class="sxs-lookup"><span data-stu-id="f0cdb-195">Example for constraint-based configurations</span></span>

<span data-ttu-id="f0cdb-196">Í þessu dæmi er notað nafnakerfi afurðarafbrigðisnúmers sem samanstendur úr eftirfarandi hlutum:</span><span class="sxs-lookup"><span data-stu-id="f0cdb-196">For this example, you use a product variant number nomenclature that consists of the following segments:</span></span>

1.  <span data-ttu-id="f0cdb-197">Númer afurðarsniðmáts</span><span class="sxs-lookup"><span data-stu-id="f0cdb-197">Product master number</span></span>
2.  <span data-ttu-id="f0cdb-198">Textafasti "\_"</span><span class="sxs-lookup"><span data-stu-id="f0cdb-198">Text constant "\_"</span></span>
3.  <span data-ttu-id="f0cdb-199">Afbrigði</span><span class="sxs-lookup"><span data-stu-id="f0cdb-199">Configuration</span></span>

<span data-ttu-id="f0cdb-200">Nafnakerfi skilgreiningar inniheldur eftirfarandi hluta:</span><span class="sxs-lookup"><span data-stu-id="f0cdb-200">The configuration nomenclature consists of the following segments:</span></span>

1.  <span data-ttu-id="f0cdb-201">Eigindargildi: Efni</span><span class="sxs-lookup"><span data-stu-id="f0cdb-201">Attribute value: Material</span></span>
2.  <span data-ttu-id="f0cdb-202">Textafasti: "AAA"</span><span class="sxs-lookup"><span data-stu-id="f0cdb-202">Text constant: "AAA"</span></span>
3.  <span data-ttu-id="f0cdb-203">Eigindargildi: Lengd</span><span class="sxs-lookup"><span data-stu-id="f0cdb-203">Attribute value: Length</span></span>

<span data-ttu-id="f0cdb-204">Hægt er að færa inn eftirfarandi gildi fyrir hluta:</span><span class="sxs-lookup"><span data-stu-id="f0cdb-204">You enter the following values for segments:</span></span>

-   <span data-ttu-id="f0cdb-205">Númer afurðarsniðmáts = **M0099**</span><span class="sxs-lookup"><span data-stu-id="f0cdb-205">Product master number = **M0099**</span></span>
-   <span data-ttu-id="f0cdb-206">Efni = **Plast**</span><span class="sxs-lookup"><span data-stu-id="f0cdb-206">Material = **Plastic**</span></span>
-   <span data-ttu-id="f0cdb-207">Lengd = **12**</span><span class="sxs-lookup"><span data-stu-id="f0cdb-207">Length = **12**</span></span>

<span data-ttu-id="f0cdb-208">Í þessu tilviki verður afurðarafbrigðisnúmerið M0099\_PlasticAAA12.</span><span class="sxs-lookup"><span data-stu-id="f0cdb-208">In this case, the product variant number will be M0099\_PlasticAAA12.</span></span>

### <a name="example-for-dimension-based-configurations"></a><span data-ttu-id="f0cdb-209">Dæmi um víddarbyggðar skilgreiningar</span><span class="sxs-lookup"><span data-stu-id="f0cdb-209">Example for dimension-based configurations</span></span>

<span data-ttu-id="f0cdb-210">Í þessu dæmi er notað nafnakerfi afurðarafbrigðisnúmers sem samanstendur úr eftirfarandi hlutum:</span><span class="sxs-lookup"><span data-stu-id="f0cdb-210">For this example, you use a product variant number nomenclature that consists of the following segments:</span></span>

1.  <span data-ttu-id="f0cdb-211">Númer afurðarsniðmáts</span><span class="sxs-lookup"><span data-stu-id="f0cdb-211">Product master number</span></span>
2.  <span data-ttu-id="f0cdb-212">Textafasti "//"</span><span class="sxs-lookup"><span data-stu-id="f0cdb-212">Text constant "//"</span></span>
3.  <span data-ttu-id="f0cdb-213">Afbrigði</span><span class="sxs-lookup"><span data-stu-id="f0cdb-213">Configuration</span></span>

<span data-ttu-id="f0cdb-214">Nafnakerfi skilgreiningar inniheldur eftirfarandi hluta:</span><span class="sxs-lookup"><span data-stu-id="f0cdb-214">The configuration nomenclature consists of the following segments:</span></span>

1.  <span data-ttu-id="f0cdb-215">Afbrigðaflokkur: Cabinet</span><span class="sxs-lookup"><span data-stu-id="f0cdb-215">Configuration group: Cabinet</span></span>
2.  <span data-ttu-id="f0cdb-216">Textafasti: "&"</span><span class="sxs-lookup"><span data-stu-id="f0cdb-216">Text constant: "&"</span></span>
3.  <span data-ttu-id="f0cdb-217">Skilgreiningaflokkur: framgrill</span><span class="sxs-lookup"><span data-stu-id="f0cdb-217">Configuration group: Front grill</span></span>

<span data-ttu-id="f0cdb-218">Hægt er að færa inn eftirfarandi gildi fyrir hluta:</span><span class="sxs-lookup"><span data-stu-id="f0cdb-218">You enter the following values for segments:</span></span>

-   <span data-ttu-id="f0cdb-219">Númer afurðarsniðmáts = **D0123**</span><span class="sxs-lookup"><span data-stu-id="f0cdb-219">Product master number = **D0123**</span></span>
-   <span data-ttu-id="f0cdb-220">Skápur = **M0008**</span><span class="sxs-lookup"><span data-stu-id="f0cdb-220">Cabinet = **M0008**</span></span>
-   <span data-ttu-id="f0cdb-221">Framhlið = **M0022**</span><span class="sxs-lookup"><span data-stu-id="f0cdb-221">Front grill = **M0022**</span></span>

<span data-ttu-id="f0cdb-222">Í þessu tilviki verður afurðarafbrigðisnúmerið D0123//M0008&M0022.</span><span class="sxs-lookup"><span data-stu-id="f0cdb-222">In this case, the product variant number will be D0123//M0008&M0022.</span></span>

## <a name="numbering-conflicts"></a><span data-ttu-id="f0cdb-223">Árekstrar númera</span><span class="sxs-lookup"><span data-stu-id="f0cdb-223">Numbering conflicts</span></span>
<span data-ttu-id="f0cdb-224">Mögulegt er að setja upp afurð nafnakerfi afurðarafbrigðisnúmers sem leiðir ekki til einkvæmra númera afurðarafbrigða.</span><span class="sxs-lookup"><span data-stu-id="f0cdb-224">In some cases, a product variant number nomenclature that you set up might not produce unique product variant numbers.</span></span> <span data-ttu-id="f0cdb-225">Til dæmis verða númer afurðarafbrigða ekki einnkvæm ef ein virk afurðarvídd er ekki innifalin í nafnakerfi fyrir afurðarsniðmát sem notar forskilgreinda tækni til skilgreiningar afbrigða.</span><span class="sxs-lookup"><span data-stu-id="f0cdb-225">For example, the product variant numbers won't be unique if one active product dimension isn't included in the nomenclature for a product master that uses the predefined variant configuration technology.</span></span> <span data-ttu-id="f0cdb-226">Aðferðin til að meðhöndla árekstra er breytileg eftir tækni við skilgreiningu.</span><span class="sxs-lookup"><span data-stu-id="f0cdb-226">The way that you handle conflicts varies, depending on the configuration technology.</span></span>

### <a name="predefined-variants"></a><span data-ttu-id="f0cdb-227">Forskilgreint afbrigði</span><span class="sxs-lookup"><span data-stu-id="f0cdb-227">Predefined variants</span></span>

<span data-ttu-id="f0cdb-228">Villa mun eiga sér stað ef reynt er að handvirkt eða sjálfkrafa mynda afurðarafbrigði þar sem eitt eða fleiri afurðarafbrigði endar á því að hafa sama númer afurðarafbrigðis.</span><span class="sxs-lookup"><span data-stu-id="f0cdb-228">An error occurs if you try to manually create or automatically generate product variants, and more than one product variant ends up with the same product variant number.</span></span> <span data-ttu-id="f0cdb-229">Til að forðast slíkt ætti frekar að nota allar virkar afurðarvíddar í afurðavíddaflokki.</span><span class="sxs-lookup"><span data-stu-id="f0cdb-229">To avoid this scenario, you should use all active product dimensions in the product dimension group.</span></span> <span data-ttu-id="f0cdb-230">Einnig er hægt að hafa með númeraröð til að tryggja enn betur að afurðarafbrigðisnúmerin séu einkvæm.</span><span class="sxs-lookup"><span data-stu-id="f0cdb-230">Alternatively, include a number sequence to help guarantee that the product variant numbers are unique.</span></span>

### <a name="constraint-based-configurations"></a><span data-ttu-id="f0cdb-231">Skorðuskilgreiningar</span><span class="sxs-lookup"><span data-stu-id="f0cdb-231">Constraint-based configurations</span></span>

<span data-ttu-id="f0cdb-232">Allt eftir nafnakerfinu getur kerfið reynt að úthluta númeri afurðarafbrigðis sem ekki er einkvæmt á skilgreiningu.</span><span class="sxs-lookup"><span data-stu-id="f0cdb-232">Depending on the nomenclature, the system might try to assign a non-unique product variant number to a configuration.</span></span> <span data-ttu-id="f0cdb-233">Í slíku tilfelli mun kerfið nota númeraröð fyrir vídd skilgreiningarvíddina sem númer afurðarafbrigðis í staðinn. Ef það gerist, mun viðvörun berast.</span><span class="sxs-lookup"><span data-stu-id="f0cdb-233">In this case, the system uses the number sequence for the configuration dimension as the product variant number instead, and you receive a warning.</span></span> <span data-ttu-id="f0cdb-234">Til að forðast slíkt ætti að taka með nógu margar eigindir í nafnakerfið til að stuðla að því að tryggja einkvæm afurðarafbrigðanúmer.</span><span class="sxs-lookup"><span data-stu-id="f0cdb-234">To avoid this scenario, you should include enough attributes in the nomenclature to help guarantee unique product variant numbers.</span></span> <span data-ttu-id="f0cdb-235">Einnig ætti að ganga úr skugga um að kveikt sé á valkostinum **Endurnota** fyrir íhlutinn.</span><span class="sxs-lookup"><span data-stu-id="f0cdb-235">You should also make sure that the **Reuse** option is turned on for the component.</span></span>

### <a name="dimension-based-configurations"></a><span data-ttu-id="f0cdb-236">Víddaskilgreiningar</span><span class="sxs-lookup"><span data-stu-id="f0cdb-236">Dimension-based configurations</span></span>

<span data-ttu-id="f0cdb-237">Á einu þrefi skilgreiningarferlisins leggur kerfið til skilgreiningargildi í samræmi við nafnakerfið.</span><span class="sxs-lookup"><span data-stu-id="f0cdb-237">During one step of the configuration process, the system suggests a configuration value according to the nomenclature.</span></span> <span data-ttu-id="f0cdb-238">Í þessu skrefi geturðu Handvirkt breytt gildi skilgreiningarinnar.</span><span class="sxs-lookup"><span data-stu-id="f0cdb-238">In this step, you can manually change the configuration value.</span></span> <span data-ttu-id="f0cdb-239">Þegar skilgreining er vistuð, mun kerfið athuga hvort gildi skilgreiningar er einkvæmt.</span><span class="sxs-lookup"><span data-stu-id="f0cdb-239">When you save the configuration, the system verifies that the configuration value is unique.</span></span> <span data-ttu-id="f0cdb-240">Ef gildið sem fært er inn er ekki einkvæmt verða send villuboð.</span><span class="sxs-lookup"><span data-stu-id="f0cdb-240">If the value that you entered isn't unique, you receive an error message.</span></span> <span data-ttu-id="f0cdb-241">Færa þarf inn gildi einkvæmrar skilgreiningar til að vista skilgreininguna.</span><span class="sxs-lookup"><span data-stu-id="f0cdb-241">To save the configuration, you must enter a unique configuration value.</span></span>

<a name="see-also"></a><span data-ttu-id="f0cdb-242">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="f0cdb-242">See also</span></span>
--------

[<span data-ttu-id="f0cdb-243">Stofna nafnakerfi afurðarnúmers fyrir fyrirframskilgreind afurðarafbrigði</span><span class="sxs-lookup"><span data-stu-id="f0cdb-243">Create a product number nomenclature for predefined product variants</span></span>](tasks/create-product-number-nomenclature-predefined-variants-2016-11.md)

[<span data-ttu-id="f0cdb-244">Stofna nafnakerfi afurðarafbrigðis fyrir skilgreind afurðarafbrigði</span><span class="sxs-lookup"><span data-stu-id="f0cdb-244">Create a product number nomenclature for configured product variants</span></span>](tasks/create-product-number-nomenclature-product-variants_2016_11.md)


