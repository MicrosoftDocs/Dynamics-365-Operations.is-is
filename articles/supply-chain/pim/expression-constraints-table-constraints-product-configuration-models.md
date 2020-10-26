---
title: Segðarskorður og töfluskorður í afbrigðalíkönum afurðar
description: Þetta efnisatriði lýsir notkun skorður segð og töfluskorðum. Skorður stjórna eigindargildin sem hægt er að velja þegar afurðir fyrir sölupöntun, sölutilboði, innkaupapöntun eða framleiðslupöntun. Hægt er að nota skorður segð eða töfluskorðum, eftir því hvernig óskað er að byggja á skorðum.
author: cvocph
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PCGlobalTableConstraintEdit, PCProductConfigurationModelDetails, PCTableConstraintAttachAttributeTree, PCTableConstraintDefinition
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 53111
ms.assetid: 5c12b1f2-eb89-4648-a755-de412f2eadd6
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: be9d9ae48d21db077928ba7bd5615fea47ea5181
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/10/2020
ms.locfileid: "3979829"
---
# <a name="expression-constraints-and-table-constraints-in-product-configuration-models"></a><span data-ttu-id="bd891-105">Segðarskorður og töfluskorður í afbrigðalíkönum afurðar</span><span class="sxs-lookup"><span data-stu-id="bd891-105">Expression constraints and table constraints in product configuration models</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bd891-106">Þetta efnisatriði lýsir notkun skorður segð og töfluskorðum.</span><span class="sxs-lookup"><span data-stu-id="bd891-106">This topic describes the use of expression constraints and table constraints.</span></span> <span data-ttu-id="bd891-107">Skorður stjórna eigindargildin sem hægt er að velja þegar afurðir fyrir sölupöntun, sölutilboði, innkaupapöntun eða framleiðslupöntun.</span><span class="sxs-lookup"><span data-stu-id="bd891-107">Constraints control the attribute values that you can select when you configure products for a sales order, sales quotation, purchase order, or production order.</span></span> <span data-ttu-id="bd891-108">Hægt er að nota skorður segð eða töfluskorðum, eftir því hvernig óskað er að byggja á skorðum.</span><span class="sxs-lookup"><span data-stu-id="bd891-108">You can use expression constraints or table constraints, depending on how you prefer to build the constraints.</span></span> 

<span data-ttu-id="bd891-109">Skorður eru notaðar til að stjórna eigindargildin sem hægt er að velja þegar afurðir fyrir sölupöntun, sölutilboði, innkaupapöntun eða framleiðslupöntun.</span><span class="sxs-lookup"><span data-stu-id="bd891-109">Constraints are used to control the attribute values that you can select when you configure products for a sales order, sales quotation, purchase order, or production order.</span></span> <span data-ttu-id="bd891-110">Hægt er að nota skorður segð eða töfluskorðum, eftir því hvernig óskað er að byggja á skorðum.</span><span class="sxs-lookup"><span data-stu-id="bd891-110">You can use expression constraints or table constraints, depending on how you prefer to build the constraints.</span></span>

## <a name="what-are-expression-constraints"></a><span data-ttu-id="bd891-111">Hvað eru segðaskorður?</span><span class="sxs-lookup"><span data-stu-id="bd891-111">What are expression constraints?</span></span>
<span data-ttu-id="bd891-112">Segð skorður eru auðkennd með segð sem notar virkjar arithmetic og Boole og aðgerðir.</span><span class="sxs-lookup"><span data-stu-id="bd891-112">Expression constraints are characterized by an expression that uses arithmetic and Boolean operators and functions.</span></span> <span data-ttu-id="bd891-113">Segðarþvingun er skrifað fyrir ákveðna íhluti í afbrigðalíkan afurðar.</span><span class="sxs-lookup"><span data-stu-id="bd891-113">An expression constraint is written for a specific component in a product configuration model.</span></span> <span data-ttu-id="bd891-114">Það er ekki hægt að endurnýta með eða deilt með öðrum íhlut.</span><span class="sxs-lookup"><span data-stu-id="bd891-114">It can't be reused by or shared with another component.</span></span> <span data-ttu-id="bd891-115">Segðarskorðurnar fyrir íhlut geta hins vegar vísað í eigindir undiríhluta íhlutarins.</span><span class="sxs-lookup"><span data-stu-id="bd891-115">However, the expression constraints for a component can reference attributes of the component's subcomponents.</span></span>

## <a name="what-are-table-constraints"></a><span data-ttu-id="bd891-116">Hvað eru töfluskorðum?</span><span class="sxs-lookup"><span data-stu-id="bd891-116">What are table constraints?</span></span>
<span data-ttu-id="bd891-117">Töfluskorður skrá samsetningargildi sem eru leyfðar fyrir eiginleika þegar þú stillir afurð.</span><span class="sxs-lookup"><span data-stu-id="bd891-117">Table constraints list the combinations of values that are allowed for attributes when you configure a product.</span></span> <span data-ttu-id="bd891-118">Skilgreiningar töfluskorðu er hægt að nota almennt.</span><span class="sxs-lookup"><span data-stu-id="bd891-118">Table constraint definitions can be used generically.</span></span> <span data-ttu-id="bd891-119">Þegar töfluskorða fyrir íhlut í afbrigðalíkani afurðar er stofnað skaltu velja skilgreiningu töfluskorðu.</span><span class="sxs-lookup"><span data-stu-id="bd891-119">When you create a table constraint for a component in a product configuration model, you select a table constraint definition.</span></span> <span data-ttu-id="bd891-120">Til að stofna samsetningar sem eru leyfðar bætirðu við eigindum ákveðinna gerða íhluta.</span><span class="sxs-lookup"><span data-stu-id="bd891-120">To create the combinations that are allowed, you add attributes of specific types to the components.</span></span> <span data-ttu-id="bd891-121">Hver gerð eigindar hefur ákveðið gildi.</span><span class="sxs-lookup"><span data-stu-id="bd891-121">Each attribute type has a specific value.</span></span>

### <a name="example-of-a-table-constraint"></a><span data-ttu-id="bd891-122">Dæmi um töfluskorðu</span><span class="sxs-lookup"><span data-stu-id="bd891-122">Example of a table constraint</span></span>

<span data-ttu-id="bd891-123">Þetta dæmi sýnir hvernig hægt er að takmarka skilgreiningu hátalara við tiltekinn frágang húss og framhliðir.</span><span class="sxs-lookup"><span data-stu-id="bd891-123">This example shows how you can limit the configuration of a speaker to specific cabinet finishes and fronts.</span></span> <span data-ttu-id="bd891-124">Fyrsta taflan sýnir frágang húss og framhliðir sem eru almennt aðgengilegar fyrir skilgreiningu.</span><span class="sxs-lookup"><span data-stu-id="bd891-124">The first table shows the cabinet finishes and fronts that are generally available for configuration.</span></span> <span data-ttu-id="bd891-125">Gildin eru skilgreind fyrir þær gerðir eiginda **frágangs húss** og **framgrills**.</span><span class="sxs-lookup"><span data-stu-id="bd891-125">The values are defined for the **Cabinet finish** and **Front grill** attribute types.</span></span>

| <span data-ttu-id="bd891-126">Gerð eigindar</span><span class="sxs-lookup"><span data-stu-id="bd891-126">Attribute type</span></span> | <span data-ttu-id="bd891-127">Gildi</span><span class="sxs-lookup"><span data-stu-id="bd891-127">Values</span></span>                      |
|----------------|-----------------------------|
| <span data-ttu-id="bd891-128">Frágangur húss</span><span class="sxs-lookup"><span data-stu-id="bd891-128">Cabinet finish</span></span> | <span data-ttu-id="bd891-129">Svart, Eik, Rósaviður, Hvítt</span><span class="sxs-lookup"><span data-stu-id="bd891-129">Black, Oak, Rosewood, White</span></span> |
| <span data-ttu-id="bd891-130">Framgrill</span><span class="sxs-lookup"><span data-stu-id="bd891-130">Front grill</span></span>    | <span data-ttu-id="bd891-131">Svart, Málmur, Hvítt</span><span class="sxs-lookup"><span data-stu-id="bd891-131">Black, Metal, White</span></span>         |

<span data-ttu-id="bd891-132">Næsta tafla sýnir samsetningar sem eru skilgreindar með töfluskorðunni **Litur og áferð**.</span><span class="sxs-lookup"><span data-stu-id="bd891-132">The next table shows the combinations that are defined by the **Color and finish** table constraint.</span></span> <span data-ttu-id="bd891-133">Með því að nota þessa töfluskorðu er hægt skilgreina hátalara sem hefur eikaráferð og svart grill, rósaviðaráferð og hvítt grill og svo framvegis.</span><span class="sxs-lookup"><span data-stu-id="bd891-133">By using this table constraint, you can configure a speaker that has an oak finish and a black grill, a Rosewood finish and a white grill, and so on.</span></span>

| <span data-ttu-id="bd891-134">Ljúk.</span><span class="sxs-lookup"><span data-stu-id="bd891-134">Finish</span></span>         | <span data-ttu-id="bd891-135">Grill</span><span class="sxs-lookup"><span data-stu-id="bd891-135">Grill</span></span>                       |
|----------------|-----------------------------|
| <span data-ttu-id="bd891-136">Eik</span><span class="sxs-lookup"><span data-stu-id="bd891-136">Oak</span></span>            | <span data-ttu-id="bd891-137">Svart</span><span class="sxs-lookup"><span data-stu-id="bd891-137">Black</span></span>                       |
| <span data-ttu-id="bd891-138">Rósaviður</span><span class="sxs-lookup"><span data-stu-id="bd891-138">Rosewood</span></span>       | <span data-ttu-id="bd891-139">Hvítt</span><span class="sxs-lookup"><span data-stu-id="bd891-139">White</span></span>                       |
| <span data-ttu-id="bd891-140">Hvítt</span><span class="sxs-lookup"><span data-stu-id="bd891-140">White</span></span>          | <span data-ttu-id="bd891-141">Svart</span><span class="sxs-lookup"><span data-stu-id="bd891-141">Black</span></span>                       |
| <span data-ttu-id="bd891-142">Hvítt</span><span class="sxs-lookup"><span data-stu-id="bd891-142">White</span></span>          | <span data-ttu-id="bd891-143">Hvítt</span><span class="sxs-lookup"><span data-stu-id="bd891-143">White</span></span>                       |
| <span data-ttu-id="bd891-144">Svart</span><span class="sxs-lookup"><span data-stu-id="bd891-144">Black</span></span>          | <span data-ttu-id="bd891-145">Svart</span><span class="sxs-lookup"><span data-stu-id="bd891-145">Black</span></span>                       |
| <span data-ttu-id="bd891-146">Svart</span><span class="sxs-lookup"><span data-stu-id="bd891-146">Black</span></span>          | <span data-ttu-id="bd891-147">Málmur</span><span class="sxs-lookup"><span data-stu-id="bd891-147">Metal</span></span>                       | 

<span data-ttu-id="bd891-148">Hægt er að stofna kerfisskilgreindar og notandaskilgreindar taflaskorður.</span><span class="sxs-lookup"><span data-stu-id="bd891-148">You can create system-defined and user-defined table constraints.</span></span> <span data-ttu-id="bd891-149">Nánari upplýsingar, sjá [Kerfisskilgreindar og notendaskilgreindar töfluskorður](system-defined-user-defined-table-constraints.md).</span><span class="sxs-lookup"><span data-stu-id="bd891-149">For more information, see [System-defined and user-defined table constraints](system-defined-user-defined-table-constraints.md).</span></span>

## <a name="what-syntax-should-be-used-to-write-constraints"></a><span data-ttu-id="bd891-150">Hvaða málskipan á að nota til að skrifa skorður?</span><span class="sxs-lookup"><span data-stu-id="bd891-150">What syntax should be used to write constraints?</span></span>
<span data-ttu-id="bd891-151">Þú verður að nota OML-málskipan (Optimization Modeling Language) þegar skorður eru skrifaðar.</span><span class="sxs-lookup"><span data-stu-id="bd891-151">You must use Optimization Modeling Language (OML) syntax when you write constraints.</span></span> <span data-ttu-id="bd891-152">Kerfið notar Microsoft Solver Foundation skorðuleysara til að leysa skorðurnar.</span><span class="sxs-lookup"><span data-stu-id="bd891-152">The system uses Microsoft Solver Foundation constraint solver to solve the constraints.</span></span>

## <a name="should-i-use-table-constraints-or-expression-constraints"></a><span data-ttu-id="bd891-153">Á ég að nota töfluskorður eða segðarskorður?</span><span class="sxs-lookup"><span data-stu-id="bd891-153">Should I use table constraints or expression constraints?</span></span>
<span data-ttu-id="bd891-154">Hægt er að nota segðarskorður eða töfluskorður, eftir því hvernig óskað er að byggja upp skorðurnar.</span><span class="sxs-lookup"><span data-stu-id="bd891-154">You can use either expression constraints or table constraints, depending on how you prefer to build the constraints.</span></span> <span data-ttu-id="bd891-155">Þú byggir upp töfluskorðu sem fylki, en segðarskorða er einstök fullyrðing.</span><span class="sxs-lookup"><span data-stu-id="bd891-155">You build a table constraint as a matrix, whereas an expression constraint is an individual statement.</span></span> <span data-ttu-id="bd891-156">Þegar þú skilgreinir vöru, þá skiptir ekki máli hvers konar þvingun er notuð.</span><span class="sxs-lookup"><span data-stu-id="bd891-156">When you configure a product, it doesn't matter what kind of constraint is used.</span></span> <span data-ttu-id="bd891-157">Eftirfarandi dæmi sýnir hvaða munur er á valkostunum tveimur.</span><span class="sxs-lookup"><span data-stu-id="bd891-157">The following example shows how the two methods differ.</span></span>  

<span data-ttu-id="bd891-158">Þegar afurð er skilgreind með því að nota eftirfarandi uppsetningar töfluskorðu eru þessar samsetningar leyfðar:</span><span class="sxs-lookup"><span data-stu-id="bd891-158">When you configure a product by using the following constraint setups, these combinations are allowed:</span></span>

-   <span data-ttu-id="bd891-159">Afurð í litnum Svart og stærð 30 eða 50</span><span class="sxs-lookup"><span data-stu-id="bd891-159">A product in the color Black, and in size 30 or 50</span></span>
-   <span data-ttu-id="bd891-160">Afurð í litnum Rautt og í stærð 20</span><span class="sxs-lookup"><span data-stu-id="bd891-160">A product in the color Red and in size 20</span></span>

### <a name="table-constraint-setup"></a><span data-ttu-id="bd891-161">Uppsetning skilgreiningar á töfluskorðu</span><span class="sxs-lookup"><span data-stu-id="bd891-161">Table constraint setup</span></span>

| <span data-ttu-id="bd891-162">Litur</span><span class="sxs-lookup"><span data-stu-id="bd891-162">Color</span></span> | <span data-ttu-id="bd891-163">Stærð</span><span class="sxs-lookup"><span data-stu-id="bd891-163">Size</span></span> |
|-------|------|
| <span data-ttu-id="bd891-164">Svart</span><span class="sxs-lookup"><span data-stu-id="bd891-164">Black</span></span> | <span data-ttu-id="bd891-165">30</span><span class="sxs-lookup"><span data-stu-id="bd891-165">30</span></span>   |
| <span data-ttu-id="bd891-166">Svart</span><span class="sxs-lookup"><span data-stu-id="bd891-166">Black</span></span> | <span data-ttu-id="bd891-167">50</span><span class="sxs-lookup"><span data-stu-id="bd891-167">50</span></span>   |
| <span data-ttu-id="bd891-168">Rautt</span><span class="sxs-lookup"><span data-stu-id="bd891-168">Red</span></span>   | <span data-ttu-id="bd891-169">20</span><span class="sxs-lookup"><span data-stu-id="bd891-169">20</span></span>   |

### <a name="expression-constraint-setup"></a><span data-ttu-id="bd891-170">Uppsetning segðarskorðu</span><span class="sxs-lookup"><span data-stu-id="bd891-170">Expression constraint setup</span></span>

<span data-ttu-id="bd891-171">(Color == "Black" & (size == "30" | size == "50")) | (color == "Red" & size = "20")</span><span class="sxs-lookup"><span data-stu-id="bd891-171">(Color == "Black" & (size == "30" | size == "50")) | (color == "Red" & size = "20")</span></span>

## <a name="should-i-use-operators-or-infix-notation-when-i-write-expression-constraints"></a><span data-ttu-id="bd891-172">Á ég nota virknitákn eða infix-tákn þegar ég að skrifa segðarskorður?</span><span class="sxs-lookup"><span data-stu-id="bd891-172">Should I use operators or infix notation when I write expression constraints?</span></span>
<span data-ttu-id="bd891-173">Hægt er að skrifa segðarskorðu með því að nota annaðhvort tiltæk forliðsvirknitákn eða infix-tákn.</span><span class="sxs-lookup"><span data-stu-id="bd891-173">You can write an expression constraint by using either the available prefix operators or infix notation.</span></span> <span data-ttu-id="bd891-174">Fyrir virknitáknin **Min**, **Max** og **Abs** er ekki hægt að nota infix-tákn.</span><span class="sxs-lookup"><span data-stu-id="bd891-174">For the **Min**, **Max**, and **Abs** operators, you can't use infix notation.</span></span> <span data-ttu-id="bd891-175">Þessi virknitákn eru tekin með sem staðaðvirknitákn í flestum forritunartungumálum.</span><span class="sxs-lookup"><span data-stu-id="bd891-175">These operators are included as standard operators in most programming languages.</span></span>

## <a name="what-operators-and-infix-notation-can-i-use-when-i-write-expression-constraints"></a><span data-ttu-id="bd891-176">Hvaða virknitákn og infix-tákn get ég notað þegar ég að skrifa segðarskorður?</span><span class="sxs-lookup"><span data-stu-id="bd891-176">What operators and infix notation can I use when I write expression constraints?</span></span>
<span data-ttu-id="bd891-177">Eftirfarandi töflur sýna virknitákn og infix-tákn sem hægt er að nota þegar segðarskorða er skrifuð fyrir íhlut í afbrigðalíkani afurðar.</span><span class="sxs-lookup"><span data-stu-id="bd891-177">The following tables list the operators and infix notation that you can use when you write an expression constraint for a component in a product configuration model.</span></span> <span data-ttu-id="bd891-178">Í dæmunum hér í fyrri töflunni er hægt að sjá hvernig á að skrifa segð með því að nota annaðhvort infix-tákn eða virknitákn.</span><span class="sxs-lookup"><span data-stu-id="bd891-178">The examples in the first table show how to write an expression by using either infix notation or operators.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="bd891-179">Virknitákn</span><span class="sxs-lookup"><span data-stu-id="bd891-179">Operator</span></span></th>
<th><span data-ttu-id="bd891-180">Lýsing</span><span class="sxs-lookup"><span data-stu-id="bd891-180">Description</span></span></th>
<th><span data-ttu-id="bd891-181">Málskipun</span><span class="sxs-lookup"><span data-stu-id="bd891-181">Syntax</span></span></th>
<th><span data-ttu-id="bd891-182">Dæmi</span><span class="sxs-lookup"><span data-stu-id="bd891-182">Examples</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="bd891-183">Felur í sér</span><span class="sxs-lookup"><span data-stu-id="bd891-183">Implies</span></span></td>
<td><span data-ttu-id="bd891-184">Þetta er satt ef fyrsta skilyrðið er rangt, annað skilyrðið er rétt, eða bæði.</span><span class="sxs-lookup"><span data-stu-id="bd891-184">This is true if the first condition is false, the second condition is true, or both.</span></span></td>
<td><span data-ttu-id="bd891-185">Felur í sér [a, b], infix: a -: b</span><span class="sxs-lookup"><span data-stu-id="bd891-185">Implies[a, b], infix: a -: b</span></span></td>
<td><ul>
<li><span data-ttu-id="bd891-186"><strong>Operator:</strong> Bendir til[x != 0, y &gt;= 0]</span><span class="sxs-lookup"><span data-stu-id="bd891-186"><strong>Operator:</strong> Implies[x != 0, y &gt;= 0]</span></span></li>
<li><span data-ttu-id="bd891-187"><strong>Infix-tákn:</strong> x != 0 -: y &gt;= 0</span><span class="sxs-lookup"><span data-stu-id="bd891-187"><strong>Infix notation:</strong> x != 0 -: y &gt;= 0</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bd891-188">Og</span><span class="sxs-lookup"><span data-stu-id="bd891-188">And</span></span></td>
<td><span data-ttu-id="bd891-189">Þetta er satt ef öll skilyrði eru uppfyllt.</span><span class="sxs-lookup"><span data-stu-id="bd891-189">This is true only if all conditions are true.</span></span> <span data-ttu-id="bd891-190">Ef skilyrði er 0 (núll), framleiðir það <strong>Rétt</strong>.</span><span class="sxs-lookup"><span data-stu-id="bd891-190">If the number of conditions is 0 (zero), it produces <strong>True</strong>.</span></span></td>
<td><span data-ttu-id="bd891-191">Og[args], infix: a &amp; b &amp; ... &amp; z</span><span class="sxs-lookup"><span data-stu-id="bd891-191">And[args], infix: a &amp; b &amp; ... &amp; z</span></span></td>
<td><ul>
<li><span data-ttu-id="bd891-192"><strong>Virknitákn:</strong> Og[x == 2, y &lt;= 2]</span><span class="sxs-lookup"><span data-stu-id="bd891-192"><strong>Operator:</strong> And[x == 2, y &lt;= 2]</span></span></li>
<li><span data-ttu-id="bd891-193"><strong>Infix-tákn:</strong> x == 2 &amp; y &lt;= 2</span><span class="sxs-lookup"><span data-stu-id="bd891-193"><strong>Infix notation:</strong> x == 2 &amp; y &lt;= 2</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bd891-194">Eða</span><span class="sxs-lookup"><span data-stu-id="bd891-194">Or</span></span></td>
<td><span data-ttu-id="bd891-195">Þetta er satt ef hvaða skilyrði er satt.</span><span class="sxs-lookup"><span data-stu-id="bd891-195">This is true if any condition is true.</span></span> <span data-ttu-id="bd891-196">Ef skilyrði er 0 (núll), framleiðir það <strong>Rangt</strong>.</span><span class="sxs-lookup"><span data-stu-id="bd891-196">If the number of conditions is 0 (zero), it produces <strong>False</strong>.</span></span></td>
<td><span data-ttu-id="bd891-197">Eða[args], infix: a | b | ... | z</span><span class="sxs-lookup"><span data-stu-id="bd891-197">Or[args], infix: a | b | ... | z</span></span></td>
<td><ul>
<li><span data-ttu-id="bd891-198"><strong>Virknitákn:</strong> Or[x == 2, y &lt;= 2]</span><span class="sxs-lookup"><span data-stu-id="bd891-198"><strong>Operator:</strong> Or[x == 2, y &lt;= 2]</span></span></li>
<li><span data-ttu-id="bd891-199"><strong>Infix-tákn:</strong> x == 2 | y &lt;= 2</span><span class="sxs-lookup"><span data-stu-id="bd891-199"><strong>Infix notation:</strong> x == 2 | y &lt;= 2</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bd891-200">Plús</span><span class="sxs-lookup"><span data-stu-id="bd891-200">Plus</span></span></td>
<td><span data-ttu-id="bd891-201">Þetta samtölur hennar skilyrði.</span><span class="sxs-lookup"><span data-stu-id="bd891-201">This sums its conditions.</span></span> <span data-ttu-id="bd891-202">Ef fjöldi skilyrða er 0 (núll), framleiðir það <strong>0</strong>.</span><span class="sxs-lookup"><span data-stu-id="bd891-202">If the number of conditions is 0 (zero), it produces <strong>0</strong>.</span></span></td>
<td><span data-ttu-id="bd891-203">Plús[args], infix: a + b + ... + z</span><span class="sxs-lookup"><span data-stu-id="bd891-203">Plus[args], infix: a + b + ... + z</span></span></td>
<td><ul>
<li><span data-ttu-id="bd891-204"><strong>Virknitákn:</strong> Plus[x, y, 2] == z</span><span class="sxs-lookup"><span data-stu-id="bd891-204"><strong>Operator:</strong> Plus[x, y, 2] == z</span></span></li>
<li><span data-ttu-id="bd891-205"><strong>Infix-tákn:</strong> x + y + 2 == z</span><span class="sxs-lookup"><span data-stu-id="bd891-205"><strong>Infix notation:</strong> x + y + 2 == z</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bd891-206">Mínus</span><span class="sxs-lookup"><span data-stu-id="bd891-206">Minus</span></span></td>
<td><span data-ttu-id="bd891-207">Þetta negates hennar frumbreytu.</span><span class="sxs-lookup"><span data-stu-id="bd891-207">This negates its argument.</span></span> <span data-ttu-id="bd891-208">Þetta verður að hafa nákvæmlega eitt skilyrði.</span><span class="sxs-lookup"><span data-stu-id="bd891-208">It must have exactly one condition.</span></span></td>
<td><span data-ttu-id="bd891-209">Mínus [expr] infix: -expr</span><span class="sxs-lookup"><span data-stu-id="bd891-209">Minus[expr], infix: -expr</span></span></td>
<td><ul>
<li><span data-ttu-id="bd891-210"><strong>Virknitákn:</strong> Minus[x] == y</span><span class="sxs-lookup"><span data-stu-id="bd891-210"><strong>Operator:</strong> Minus[x] == y</span></span></li>
<li><span data-ttu-id="bd891-211"><strong>Infix-tákn:</strong> -x == y</span><span class="sxs-lookup"><span data-stu-id="bd891-211"><strong>Infix notation:</strong> -x == y</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bd891-212">Abs</span><span class="sxs-lookup"><span data-stu-id="bd891-212">Abs</span></span></td>
<td><span data-ttu-id="bd891-213">Þetta tekur raungildi hennar skilyrði.</span><span class="sxs-lookup"><span data-stu-id="bd891-213">This takes the absolute value of its condition.</span></span> <span data-ttu-id="bd891-214">Þetta verður að hafa nákvæmlega eitt skilyrði.</span><span class="sxs-lookup"><span data-stu-id="bd891-214">It must have exactly one condition.</span></span></td>
<td><span data-ttu-id="bd891-215">[Expr] abs</span><span class="sxs-lookup"><span data-stu-id="bd891-215">Abs[expr]</span></span></td>
<td><span data-ttu-id="bd891-216"><strong>Virknitákn:</strong> Abs[x]</span><span class="sxs-lookup"><span data-stu-id="bd891-216"><strong>Operator:</strong> Abs[x]</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bd891-217">Tímar</span><span class="sxs-lookup"><span data-stu-id="bd891-217">Times</span></span></td>
<td><span data-ttu-id="bd891-218">Þetta tekur afurðar þess skilyrða.</span><span class="sxs-lookup"><span data-stu-id="bd891-218">This takes the product of its conditions.</span></span> <span data-ttu-id="bd891-219">Ef fjöldi skilyrða er 0 (núll), framleiðir það <strong>1</strong>.</span><span class="sxs-lookup"><span data-stu-id="bd891-219">If the number of conditions is 0 (zero), it produces <strong>1</strong>.</span></span></td>
<td><span data-ttu-id="bd891-220">Sinnum[args], infix: a \* b \* ... \* z</span><span class="sxs-lookup"><span data-stu-id="bd891-220">Times[args], infix: a \* b \* ... \* z</span></span></td>
<td><ul>
<li><span data-ttu-id="bd891-221"><strong>Virknitákn:</strong> Times[x, y, 2] == z</span><span class="sxs-lookup"><span data-stu-id="bd891-221"><strong>Operator:</strong> Times[x, y, 2] == z</span></span></li>
<li><span data-ttu-id="bd891-222"><strong>Infix-tákn:</strong> x \* y \* 2 == z</span><span class="sxs-lookup"><span data-stu-id="bd891-222"><strong>Infix notation:</strong> x \* y \* 2 == z</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bd891-223">Styrkur</span><span class="sxs-lookup"><span data-stu-id="bd891-223">Power</span></span></td>
<td><span data-ttu-id="bd891-224">Þetta tekur til exponential.</span><span class="sxs-lookup"><span data-stu-id="bd891-224">This takes an exponential.</span></span> <span data-ttu-id="bd891-225">Þetta á við veldi frá hægri til vinstri.</span><span class="sxs-lookup"><span data-stu-id="bd891-225">It applies exponentiation from right to left.</span></span> <span data-ttu-id="bd891-226">(Með öðrum orðum &#39; hægri-tengt.) Þess vegna er <strong>Power[a, b, c]</strong> jafnt og <strong>Power[a, Power[b, c]]</strong>.</span><span class="sxs-lookup"><span data-stu-id="bd891-226">(In other words, it&#39;s right-associative.) Therefore, <strong>Power[a, b, c]</strong> is equivalent to <strong>Power[a, Power[b, c]]</strong>.</span></span> <span data-ttu-id="bd891-227"><strong>Afl</strong> er aðeins hægt að nota með jákvæða fasta sem veldisvísi.</span><span class="sxs-lookup"><span data-stu-id="bd891-227"><strong>Power</strong> can be used only if the exponent is a positive constant.</span></span></td>
<td><span data-ttu-id="bd891-228">Power[args], infix: a ^ b ^ ... ^ z</span><span class="sxs-lookup"><span data-stu-id="bd891-228">Power[args], infix: a ^ b ^ ... ^ z</span></span></td>
<td><ul>
<li><span data-ttu-id="bd891-229"><strong>Virknitákn:</strong> Power[x, 2] == y</span><span class="sxs-lookup"><span data-stu-id="bd891-229"><strong>Operator:</strong> Power[x, 2] == y</span></span></li>
<li><span data-ttu-id="bd891-230"><strong>Infix-tákn:</strong> x ^ 2 == y</span><span class="sxs-lookup"><span data-stu-id="bd891-230"><strong>Infix notation:</strong> x ^ 2 == y</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bd891-231">Hámark</span><span class="sxs-lookup"><span data-stu-id="bd891-231">Max</span></span></td>
<td><span data-ttu-id="bd891-232">Þetta myndar stærsta skilyrðið.</span><span class="sxs-lookup"><span data-stu-id="bd891-232">This produces the largest condition.</span></span> <span data-ttu-id="bd891-233">Ef fjöldi skilyrða er 0 (núll), framleiðir það <strong>Óendanleiki</strong>.</span><span class="sxs-lookup"><span data-stu-id="bd891-233">If the number of conditions is 0 (zero), it produces <strong>Infinity</strong>.</span></span></td>
<td><span data-ttu-id="bd891-234">Max [viðföng]</span><span class="sxs-lookup"><span data-stu-id="bd891-234">Max[args]</span></span></td>
<td><span data-ttu-id="bd891-235"><strong>Virknitákn:</strong> Max[x, y, 2] == z</span><span class="sxs-lookup"><span data-stu-id="bd891-235"><strong>Operator:</strong> Max[x, y, 2] == z</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bd891-236">Lágmark</span><span class="sxs-lookup"><span data-stu-id="bd891-236">Min</span></span></td>
<td><span data-ttu-id="bd891-237">Þetta birtir lægstu skilyrði.</span><span class="sxs-lookup"><span data-stu-id="bd891-237">This produces the smallest condition.</span></span> <span data-ttu-id="bd891-238">Ef fjöldi skilyrða er 0 (núll), framleiðir það <strong>Óendanleiki</strong>.</span><span class="sxs-lookup"><span data-stu-id="bd891-238">If the number of conditions is 0 (zero), it produces <strong>Infinity</strong>.</span></span></td>
<td><span data-ttu-id="bd891-239">Mín. [viðföng]</span><span class="sxs-lookup"><span data-stu-id="bd891-239">Min[args]</span></span></td>
<td><span data-ttu-id="bd891-240"><strong>Virknitákn:</strong> Min[x, y, 2] == z</span><span class="sxs-lookup"><span data-stu-id="bd891-240"><strong>Operator:</strong> Min[x, y, 2] == z</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bd891-241">Ekki</span><span class="sxs-lookup"><span data-stu-id="bd891-241">Not</span></span></td>
<td><span data-ttu-id="bd891-242">Þetta myndar röklegt inverse skilyrðis hennar.</span><span class="sxs-lookup"><span data-stu-id="bd891-242">This produces the logical inverse of its condition.</span></span> <span data-ttu-id="bd891-243">Þetta verður að hafa nákvæmlega eitt skilyrði.</span><span class="sxs-lookup"><span data-stu-id="bd891-243">It must have exactly one condition.</span></span></td>
<td><span data-ttu-id="bd891-244">Ekki [expr] infix: expr</span><span class="sxs-lookup"><span data-stu-id="bd891-244">Not[expr], infix: !expr</span></span></td>
<td><ul>
<li><span data-ttu-id="bd891-245"><strong>Virknitákn:</strong> Ekki[x] &amp; Ekki[y == 3]</span><span class="sxs-lookup"><span data-stu-id="bd891-245"><strong>Operator:</strong> Not[x] &amp; Not[y == 3]</span></span></li>
<li><span data-ttu-id="bd891-246"><strong>Infix-tákn:</strong> !x!(y == 3)</span><span class="sxs-lookup"><span data-stu-id="bd891-246"><strong>Infix notation:</strong> !x!(y == 3)</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

<span data-ttu-id="bd891-247">Dæmi í næstu töflu sýna hvernig á að skrifa infix-tákn.</span><span class="sxs-lookup"><span data-stu-id="bd891-247">The examples in the next table show how to write infix notation.</span></span>


|  <span data-ttu-id="bd891-248">Infix merki</span><span class="sxs-lookup"><span data-stu-id="bd891-248">Infix notation</span></span>   |                                          <span data-ttu-id="bd891-249">lýsing</span><span class="sxs-lookup"><span data-stu-id="bd891-249">Description</span></span>                                          |
|-------------------|-----------------------------------------------------------------------------------------------|
|     <span data-ttu-id="bd891-250">x + y + z</span><span class="sxs-lookup"><span data-stu-id="bd891-250">x + y + z</span></span>     |                                           <span data-ttu-id="bd891-251">samlagning</span><span class="sxs-lookup"><span data-stu-id="bd891-251">Addition</span></span>                                            |
|    <span data-ttu-id="bd891-252">x \* y \* z</span><span class="sxs-lookup"><span data-stu-id="bd891-252">x \* y \* z</span></span>    |                                        <span data-ttu-id="bd891-253">Margföldun</span><span class="sxs-lookup"><span data-stu-id="bd891-253">Multiplication</span></span>                                         |
|       <span data-ttu-id="bd891-254">x - y</span><span class="sxs-lookup"><span data-stu-id="bd891-254">x - y</span></span>       | <span data-ttu-id="bd891-255">Frádráttur tvíundakerfis er umreiknaður eins og viðbót tvíundakerfis þar sem er neitaða aðra.</span><span class="sxs-lookup"><span data-stu-id="bd891-255">Binary subtraction is translated the same as binary addition where there is a negated second.</span></span> |
|     <span data-ttu-id="bd891-256">x ^ y ^ z</span><span class="sxs-lookup"><span data-stu-id="bd891-256">x ^ y ^ z</span></span>     |                          <span data-ttu-id="bd891-257">Veldi sem hefur hægri tengslavirkni</span><span class="sxs-lookup"><span data-stu-id="bd891-257">Exponentiation that has right associativity</span></span>                          |
|        <span data-ttu-id="bd891-258">!x</span><span class="sxs-lookup"><span data-stu-id="bd891-258">!x</span></span>         |                                          <span data-ttu-id="bd891-259">Boole-ekki</span><span class="sxs-lookup"><span data-stu-id="bd891-259">Boolean not</span></span>                                          |
|      <span data-ttu-id="bd891-260">x -: y</span><span class="sxs-lookup"><span data-stu-id="bd891-260">x -: y</span></span>       |                                      <span data-ttu-id="bd891-261">Boole-leiðing</span><span class="sxs-lookup"><span data-stu-id="bd891-261">Boolean implication</span></span>                                      |
|         <span data-ttu-id="bd891-262">x</span><span class="sxs-lookup"><span data-stu-id="bd891-262">x</span></span>         |                                               <span data-ttu-id="bd891-263">y</span><span class="sxs-lookup"><span data-stu-id="bd891-263">y</span></span>                                               |
|     <span data-ttu-id="bd891-264">x & y & z</span><span class="sxs-lookup"><span data-stu-id="bd891-264">x & y & z</span></span>     |                                          <span data-ttu-id="bd891-265">Boole- og</span><span class="sxs-lookup"><span data-stu-id="bd891-265">Boolean and</span></span>                                          |
|    <span data-ttu-id="bd891-266">x == y == z</span><span class="sxs-lookup"><span data-stu-id="bd891-266">x == y == z</span></span>    |                                           <span data-ttu-id="bd891-267">Jafngildi</span><span class="sxs-lookup"><span data-stu-id="bd891-267">Equality</span></span>                                            |
|    <span data-ttu-id="bd891-268">x != y != z</span><span class="sxs-lookup"><span data-stu-id="bd891-268">x != y != z</span></span>    |                                           <span data-ttu-id="bd891-269">Ákveðið</span><span class="sxs-lookup"><span data-stu-id="bd891-269">Distinct</span></span>                                            |
|  <span data-ttu-id="bd891-270">x &lt; y &lt; z</span><span class="sxs-lookup"><span data-stu-id="bd891-270">x &lt; y &lt; z</span></span>  |                                           <span data-ttu-id="bd891-271">Minna en</span><span class="sxs-lookup"><span data-stu-id="bd891-271">Less than</span></span>                                           |
|  <span data-ttu-id="bd891-272">x &gt; y &gt; z</span><span class="sxs-lookup"><span data-stu-id="bd891-272">x &gt; y &gt; z</span></span>  |                                         <span data-ttu-id="bd891-273">Stærra en</span><span class="sxs-lookup"><span data-stu-id="bd891-273">Greater than</span></span>                                          |
| <span data-ttu-id="bd891-274">x &lt;= y &lt;= z</span><span class="sxs-lookup"><span data-stu-id="bd891-274">x &lt;= y &lt;= z</span></span> |                                     <span data-ttu-id="bd891-275">Minna en eða jafnt og</span><span class="sxs-lookup"><span data-stu-id="bd891-275">Less than or equal to</span></span>                                     |
| <span data-ttu-id="bd891-276">x &gt;= y &gt;= z</span><span class="sxs-lookup"><span data-stu-id="bd891-276">x &gt;= y &gt;= z</span></span> |                                   <span data-ttu-id="bd891-277">Stærra en eða jafnt og</span><span class="sxs-lookup"><span data-stu-id="bd891-277">Greater than or equal to</span></span>                                    |
|        <span data-ttu-id="bd891-278">(x)</span><span class="sxs-lookup"><span data-stu-id="bd891-278">(x)</span></span>        |                           <span data-ttu-id="bd891-279">Svigaar hnekkja sjálfgefinn forgang.</span><span class="sxs-lookup"><span data-stu-id="bd891-279">Parentheses override default precedence.</span></span>                            |

## <a name="why-arent-my-expression-constraints-validated-correctly"></a><span data-ttu-id="bd891-280">Af hverju eru mínar segðaskorður ekki sannprófaðar rétt?</span><span class="sxs-lookup"><span data-stu-id="bd891-280">Why aren't my expression constraints validated correctly?</span></span>
<span data-ttu-id="bd891-281">Frátekið lykilorð er hægt að nota sem heiti leysara eigindir, íhluti eða undiríhlutir í afbrigðalíkani afurðar.</span><span class="sxs-lookup"><span data-stu-id="bd891-281">You can't use reserved keywords as solver names for attributes, components, or subcomponents in a product configuration model.</span></span><span data-ttu-id="bd891-282"> Hér er listi yfir frátekin lykilorð sem ekki er hægt að nota:</span><span class="sxs-lookup"><span data-stu-id="bd891-282"> Here is a list of the reserved keywords that you can't use:</span></span>

-   <span data-ttu-id="bd891-283">Þak</span><span class="sxs-lookup"><span data-stu-id="bd891-283">Ceiling</span></span>
-   <span data-ttu-id="bd891-284">Eining</span><span class="sxs-lookup"><span data-stu-id="bd891-284">Element</span></span>
-   <span data-ttu-id="bd891-285">Jafnt</span><span class="sxs-lookup"><span data-stu-id="bd891-285">Equal</span></span>
-   <span data-ttu-id="bd891-286">Hæð</span><span class="sxs-lookup"><span data-stu-id="bd891-286">Floor</span></span>
-   <span data-ttu-id="bd891-287">Ef</span><span class="sxs-lookup"><span data-stu-id="bd891-287">If</span></span>
-   <span data-ttu-id="bd891-288">Minna</span><span class="sxs-lookup"><span data-stu-id="bd891-288">Less</span></span>
-   <span data-ttu-id="bd891-289">Hærri</span><span class="sxs-lookup"><span data-stu-id="bd891-289">Greater</span></span>
-   <span data-ttu-id="bd891-290">Felur í sér</span><span class="sxs-lookup"><span data-stu-id="bd891-290">Implies</span></span>
-   <span data-ttu-id="bd891-291">Kladdi</span><span class="sxs-lookup"><span data-stu-id="bd891-291">Log</span></span>
-   <span data-ttu-id="bd891-292">Hám.</span><span class="sxs-lookup"><span data-stu-id="bd891-292">Max</span></span>
-   <span data-ttu-id="bd891-293">Mín.</span><span class="sxs-lookup"><span data-stu-id="bd891-293">Min</span></span>
-   <span data-ttu-id="bd891-294">Mínus</span><span class="sxs-lookup"><span data-stu-id="bd891-294">Minus</span></span>
-   <span data-ttu-id="bd891-295">Plús</span><span class="sxs-lookup"><span data-stu-id="bd891-295">Plus</span></span>
-   <span data-ttu-id="bd891-296">Styrkur</span><span class="sxs-lookup"><span data-stu-id="bd891-296">Power</span></span>
-   <span data-ttu-id="bd891-297">Tímar</span><span class="sxs-lookup"><span data-stu-id="bd891-297">Times</span></span>
-   <span data-ttu-id="bd891-298">Rauf</span><span class="sxs-lookup"><span data-stu-id="bd891-298">Slot</span></span>
-   <span data-ttu-id="bd891-299">Tegund</span><span class="sxs-lookup"><span data-stu-id="bd891-299">Model</span></span>
-   <span data-ttu-id="bd891-300">Ákvörðun</span><span class="sxs-lookup"><span data-stu-id="bd891-300">Decision</span></span>
-   <span data-ttu-id="bd891-301">Markmið</span><span class="sxs-lookup"><span data-stu-id="bd891-301">Goal</span></span>


<a name="additional-resources"></a><span data-ttu-id="bd891-302">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="bd891-302">Additional resources</span></span>
--------

[<span data-ttu-id="bd891-303">Stofna segð töfluskorðu</span><span class="sxs-lookup"><span data-stu-id="bd891-303">Create an expression constraint</span></span>](tasks/add-expression-constraint-product-configuration-model.md)

[<span data-ttu-id="bd891-304">Bæta útreikningi við afbrigðalíkan afurðar</span><span class="sxs-lookup"><span data-stu-id="bd891-304">Add a calculation to a product configuration model</span></span>](tasks/add-calculation-product-configuration-model.md)



