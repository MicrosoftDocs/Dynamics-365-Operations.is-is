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
ms.custom: 53111
ms.assetid: 5c12b1f2-eb89-4648-a755-de412f2eadd6
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bc07d5b915e0b878cc7b2ef1d5f3253de8776608
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "5007706"
---
# <a name="expression-constraints-and-table-constraints-in-product-configuration-models"></a><span data-ttu-id="68b13-105">Segðarskorður og töfluskorður í afbrigðalíkönum afurðar</span><span class="sxs-lookup"><span data-stu-id="68b13-105">Expression constraints and table constraints in product configuration models</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="68b13-106">Þetta efnisatriði lýsir notkun skorður segð og töfluskorðum.</span><span class="sxs-lookup"><span data-stu-id="68b13-106">This topic describes the use of expression constraints and table constraints.</span></span> <span data-ttu-id="68b13-107">Skorður stjórna eigindargildin sem hægt er að velja þegar afurðir fyrir sölupöntun, sölutilboði, innkaupapöntun eða framleiðslupöntun.</span><span class="sxs-lookup"><span data-stu-id="68b13-107">Constraints control the attribute values that you can select when you configure products for a sales order, sales quotation, purchase order, or production order.</span></span> <span data-ttu-id="68b13-108">Hægt er að nota skorður segð eða töfluskorðum, eftir því hvernig óskað er að byggja á skorðum.</span><span class="sxs-lookup"><span data-stu-id="68b13-108">You can use expression constraints or table constraints, depending on how you prefer to build the constraints.</span></span> 

<span data-ttu-id="68b13-109">Skorður eru notaðar til að stjórna eigindargildin sem hægt er að velja þegar afurðir fyrir sölupöntun, sölutilboði, innkaupapöntun eða framleiðslupöntun.</span><span class="sxs-lookup"><span data-stu-id="68b13-109">Constraints are used to control the attribute values that you can select when you configure products for a sales order, sales quotation, purchase order, or production order.</span></span> <span data-ttu-id="68b13-110">Hægt er að nota skorður segð eða töfluskorðum, eftir því hvernig óskað er að byggja á skorðum.</span><span class="sxs-lookup"><span data-stu-id="68b13-110">You can use expression constraints or table constraints, depending on how you prefer to build the constraints.</span></span>

## <a name="what-are-expression-constraints"></a><span data-ttu-id="68b13-111">Hvað eru segðaskorður?</span><span class="sxs-lookup"><span data-stu-id="68b13-111">What are expression constraints?</span></span>
<span data-ttu-id="68b13-112">Segð skorður eru auðkennd með segð sem notar virkjar arithmetic og Boole og aðgerðir.</span><span class="sxs-lookup"><span data-stu-id="68b13-112">Expression constraints are characterized by an expression that uses arithmetic and Boolean operators and functions.</span></span> <span data-ttu-id="68b13-113">Segðarþvingun er skrifað fyrir ákveðna íhluti í afbrigðalíkan afurðar.</span><span class="sxs-lookup"><span data-stu-id="68b13-113">An expression constraint is written for a specific component in a product configuration model.</span></span> <span data-ttu-id="68b13-114">Það er ekki hægt að endurnýta með eða deilt með öðrum íhlut.</span><span class="sxs-lookup"><span data-stu-id="68b13-114">It can't be reused by or shared with another component.</span></span> <span data-ttu-id="68b13-115">Segðarskorðurnar fyrir íhlut geta hins vegar vísað í eigindir undiríhluta íhlutarins.</span><span class="sxs-lookup"><span data-stu-id="68b13-115">However, the expression constraints for a component can reference attributes of the component's subcomponents.</span></span>

## <a name="what-are-table-constraints"></a><span data-ttu-id="68b13-116">Hvað eru töfluskorðum?</span><span class="sxs-lookup"><span data-stu-id="68b13-116">What are table constraints?</span></span>
<span data-ttu-id="68b13-117">Töfluskorður skrá samsetningargildi sem eru leyfðar fyrir eiginleika þegar þú stillir afurð.</span><span class="sxs-lookup"><span data-stu-id="68b13-117">Table constraints list the combinations of values that are allowed for attributes when you configure a product.</span></span> <span data-ttu-id="68b13-118">Skilgreiningar töfluskorðu er hægt að nota almennt.</span><span class="sxs-lookup"><span data-stu-id="68b13-118">Table constraint definitions can be used generically.</span></span> <span data-ttu-id="68b13-119">Þegar töfluskorða fyrir íhlut í afbrigðalíkani afurðar er stofnað skaltu velja skilgreiningu töfluskorðu.</span><span class="sxs-lookup"><span data-stu-id="68b13-119">When you create a table constraint for a component in a product configuration model, you select a table constraint definition.</span></span> <span data-ttu-id="68b13-120">Til að stofna samsetningar sem eru leyfðar bætirðu við eigindum ákveðinna gerða íhluta.</span><span class="sxs-lookup"><span data-stu-id="68b13-120">To create the combinations that are allowed, you add attributes of specific types to the components.</span></span> <span data-ttu-id="68b13-121">Hver gerð eigindar hefur ákveðið gildi.</span><span class="sxs-lookup"><span data-stu-id="68b13-121">Each attribute type has a specific value.</span></span>

### <a name="example-of-a-table-constraint"></a><span data-ttu-id="68b13-122">Dæmi um töfluskorðu</span><span class="sxs-lookup"><span data-stu-id="68b13-122">Example of a table constraint</span></span>

<span data-ttu-id="68b13-123">Þetta dæmi sýnir hvernig hægt er að takmarka skilgreiningu hátalara við tiltekinn frágang húss og framhliðir.</span><span class="sxs-lookup"><span data-stu-id="68b13-123">This example shows how you can limit the configuration of a speaker to specific cabinet finishes and fronts.</span></span> <span data-ttu-id="68b13-124">Fyrsta taflan sýnir frágang húss og framhliðir sem eru almennt aðgengilegar fyrir skilgreiningu.</span><span class="sxs-lookup"><span data-stu-id="68b13-124">The first table shows the cabinet finishes and fronts that are generally available for configuration.</span></span> <span data-ttu-id="68b13-125">Gildin eru skilgreind fyrir þær gerðir eiginda **frágangs húss** og **framgrills**.</span><span class="sxs-lookup"><span data-stu-id="68b13-125">The values are defined for the **Cabinet finish** and **Front grill** attribute types.</span></span>

| <span data-ttu-id="68b13-126">Gerð eigindar</span><span class="sxs-lookup"><span data-stu-id="68b13-126">Attribute type</span></span> | <span data-ttu-id="68b13-127">Gildi</span><span class="sxs-lookup"><span data-stu-id="68b13-127">Values</span></span>                      |
|----------------|-----------------------------|
| <span data-ttu-id="68b13-128">Frágangur húss</span><span class="sxs-lookup"><span data-stu-id="68b13-128">Cabinet finish</span></span> | <span data-ttu-id="68b13-129">Svart, Eik, Rósaviður, Hvítt</span><span class="sxs-lookup"><span data-stu-id="68b13-129">Black, Oak, Rosewood, White</span></span> |
| <span data-ttu-id="68b13-130">Framgrill</span><span class="sxs-lookup"><span data-stu-id="68b13-130">Front grill</span></span>    | <span data-ttu-id="68b13-131">Svart, Málmur, Hvítt</span><span class="sxs-lookup"><span data-stu-id="68b13-131">Black, Metal, White</span></span>         |

<span data-ttu-id="68b13-132">Næsta tafla sýnir samsetningar sem eru skilgreindar með töfluskorðunni **Litur og áferð**.</span><span class="sxs-lookup"><span data-stu-id="68b13-132">The next table shows the combinations that are defined by the **Color and finish** table constraint.</span></span> <span data-ttu-id="68b13-133">Með því að nota þessa töfluskorðu er hægt skilgreina hátalara sem hefur eikaráferð og svart grill, rósaviðaráferð og hvítt grill og svo framvegis.</span><span class="sxs-lookup"><span data-stu-id="68b13-133">By using this table constraint, you can configure a speaker that has an oak finish and a black grill, a Rosewood finish and a white grill, and so on.</span></span>

| <span data-ttu-id="68b13-134">Ljúk.</span><span class="sxs-lookup"><span data-stu-id="68b13-134">Finish</span></span>         | <span data-ttu-id="68b13-135">Grill</span><span class="sxs-lookup"><span data-stu-id="68b13-135">Grill</span></span>                       |
|----------------|-----------------------------|
| <span data-ttu-id="68b13-136">Eik</span><span class="sxs-lookup"><span data-stu-id="68b13-136">Oak</span></span>            | <span data-ttu-id="68b13-137">Svart</span><span class="sxs-lookup"><span data-stu-id="68b13-137">Black</span></span>                       |
| <span data-ttu-id="68b13-138">Rósaviður</span><span class="sxs-lookup"><span data-stu-id="68b13-138">Rosewood</span></span>       | <span data-ttu-id="68b13-139">Hvítt</span><span class="sxs-lookup"><span data-stu-id="68b13-139">White</span></span>                       |
| <span data-ttu-id="68b13-140">Hvítt</span><span class="sxs-lookup"><span data-stu-id="68b13-140">White</span></span>          | <span data-ttu-id="68b13-141">Svart</span><span class="sxs-lookup"><span data-stu-id="68b13-141">Black</span></span>                       |
| <span data-ttu-id="68b13-142">Hvítt</span><span class="sxs-lookup"><span data-stu-id="68b13-142">White</span></span>          | <span data-ttu-id="68b13-143">Hvítt</span><span class="sxs-lookup"><span data-stu-id="68b13-143">White</span></span>                       |
| <span data-ttu-id="68b13-144">Svart</span><span class="sxs-lookup"><span data-stu-id="68b13-144">Black</span></span>          | <span data-ttu-id="68b13-145">Svart</span><span class="sxs-lookup"><span data-stu-id="68b13-145">Black</span></span>                       |
| <span data-ttu-id="68b13-146">Svart</span><span class="sxs-lookup"><span data-stu-id="68b13-146">Black</span></span>          | <span data-ttu-id="68b13-147">Málmur</span><span class="sxs-lookup"><span data-stu-id="68b13-147">Metal</span></span>                       | 

<span data-ttu-id="68b13-148">Hægt er að stofna kerfisskilgreindar og notandaskilgreindar taflaskorður.</span><span class="sxs-lookup"><span data-stu-id="68b13-148">You can create system-defined and user-defined table constraints.</span></span> <span data-ttu-id="68b13-149">Nánari upplýsingar, sjá [Kerfisskilgreindar og notendaskilgreindar töfluskorður](system-defined-user-defined-table-constraints.md).</span><span class="sxs-lookup"><span data-stu-id="68b13-149">For more information, see [System-defined and user-defined table constraints](system-defined-user-defined-table-constraints.md).</span></span>

## <a name="what-syntax-should-be-used-to-write-constraints"></a><span data-ttu-id="68b13-150">Hvaða málskipan á að nota til að skrifa skorður?</span><span class="sxs-lookup"><span data-stu-id="68b13-150">What syntax should be used to write constraints?</span></span>
<span data-ttu-id="68b13-151">Þú verður að nota OML-málskipan (Optimization Modeling Language) þegar skorður eru skrifaðar.</span><span class="sxs-lookup"><span data-stu-id="68b13-151">You must use Optimization Modeling Language (OML) syntax when you write constraints.</span></span> <span data-ttu-id="68b13-152">Kerfið notar Microsoft Solver Foundation skorðuleysara til að leysa skorðurnar.</span><span class="sxs-lookup"><span data-stu-id="68b13-152">The system uses Microsoft Solver Foundation constraint solver to solve the constraints.</span></span>

## <a name="should-i-use-table-constraints-or-expression-constraints"></a><span data-ttu-id="68b13-153">Á ég að nota töfluskorður eða segðarskorður?</span><span class="sxs-lookup"><span data-stu-id="68b13-153">Should I use table constraints or expression constraints?</span></span>
<span data-ttu-id="68b13-154">Hægt er að nota segðarskorður eða töfluskorður, eftir því hvernig óskað er að byggja upp skorðurnar.</span><span class="sxs-lookup"><span data-stu-id="68b13-154">You can use either expression constraints or table constraints, depending on how you prefer to build the constraints.</span></span> <span data-ttu-id="68b13-155">Þú byggir upp töfluskorðu sem fylki, en segðarskorða er einstök fullyrðing.</span><span class="sxs-lookup"><span data-stu-id="68b13-155">You build a table constraint as a matrix, whereas an expression constraint is an individual statement.</span></span> <span data-ttu-id="68b13-156">Þegar þú skilgreinir vöru, þá skiptir ekki máli hvers konar þvingun er notuð.</span><span class="sxs-lookup"><span data-stu-id="68b13-156">When you configure a product, it doesn't matter what kind of constraint is used.</span></span> <span data-ttu-id="68b13-157">Eftirfarandi dæmi sýnir hvaða munur er á valkostunum tveimur.</span><span class="sxs-lookup"><span data-stu-id="68b13-157">The following example shows how the two methods differ.</span></span>  

<span data-ttu-id="68b13-158">Þegar afurð er skilgreind með því að nota eftirfarandi uppsetningar töfluskorðu eru þessar samsetningar leyfðar:</span><span class="sxs-lookup"><span data-stu-id="68b13-158">When you configure a product by using the following constraint setups, these combinations are allowed:</span></span>

-   <span data-ttu-id="68b13-159">Afurð í litnum Svart og stærð 30 eða 50</span><span class="sxs-lookup"><span data-stu-id="68b13-159">A product in the color Black, and in size 30 or 50</span></span>
-   <span data-ttu-id="68b13-160">Afurð í litnum Rautt og í stærð 20</span><span class="sxs-lookup"><span data-stu-id="68b13-160">A product in the color Red and in size 20</span></span>

### <a name="table-constraint-setup"></a><span data-ttu-id="68b13-161">Uppsetning skilgreiningar á töfluskorðu</span><span class="sxs-lookup"><span data-stu-id="68b13-161">Table constraint setup</span></span>

| <span data-ttu-id="68b13-162">Litur</span><span class="sxs-lookup"><span data-stu-id="68b13-162">Color</span></span> | <span data-ttu-id="68b13-163">Stærð</span><span class="sxs-lookup"><span data-stu-id="68b13-163">Size</span></span> |
|-------|------|
| <span data-ttu-id="68b13-164">Svart</span><span class="sxs-lookup"><span data-stu-id="68b13-164">Black</span></span> | <span data-ttu-id="68b13-165">30</span><span class="sxs-lookup"><span data-stu-id="68b13-165">30</span></span>   |
| <span data-ttu-id="68b13-166">Svart</span><span class="sxs-lookup"><span data-stu-id="68b13-166">Black</span></span> | <span data-ttu-id="68b13-167">50</span><span class="sxs-lookup"><span data-stu-id="68b13-167">50</span></span>   |
| <span data-ttu-id="68b13-168">Rautt</span><span class="sxs-lookup"><span data-stu-id="68b13-168">Red</span></span>   | <span data-ttu-id="68b13-169">20</span><span class="sxs-lookup"><span data-stu-id="68b13-169">20</span></span>   |

### <a name="expression-constraint-setup"></a><span data-ttu-id="68b13-170">Uppsetning segðarskorðu</span><span class="sxs-lookup"><span data-stu-id="68b13-170">Expression constraint setup</span></span>

<span data-ttu-id="68b13-171">(Color == "Black" & (size == "30" | size == "50")) | (color == "Red" & size = "20")</span><span class="sxs-lookup"><span data-stu-id="68b13-171">(Color == "Black" & (size == "30" | size == "50")) | (color == "Red" & size = "20")</span></span>

## <a name="should-i-use-operators-or-infix-notation-when-i-write-expression-constraints"></a><span data-ttu-id="68b13-172">Á ég nota virknitákn eða infix-tákn þegar ég að skrifa segðarskorður?</span><span class="sxs-lookup"><span data-stu-id="68b13-172">Should I use operators or infix notation when I write expression constraints?</span></span>
<span data-ttu-id="68b13-173">Hægt er að skrifa segðarskorðu með því að nota annaðhvort tiltæk forliðsvirknitákn eða infix-tákn.</span><span class="sxs-lookup"><span data-stu-id="68b13-173">You can write an expression constraint by using either the available prefix operators or infix notation.</span></span> <span data-ttu-id="68b13-174">Fyrir virknitáknin **Min**, **Max** og **Abs** er ekki hægt að nota infix-tákn.</span><span class="sxs-lookup"><span data-stu-id="68b13-174">For the **Min**, **Max**, and **Abs** operators, you can't use infix notation.</span></span> <span data-ttu-id="68b13-175">Þessi virknitákn eru tekin með sem staðaðvirknitákn í flestum forritunartungumálum.</span><span class="sxs-lookup"><span data-stu-id="68b13-175">These operators are included as standard operators in most programming languages.</span></span>

## <a name="what-operators-and-infix-notation-can-i-use-when-i-write-expression-constraints"></a><span data-ttu-id="68b13-176">Hvaða virknitákn og infix-tákn get ég notað þegar ég að skrifa segðarskorður?</span><span class="sxs-lookup"><span data-stu-id="68b13-176">What operators and infix notation can I use when I write expression constraints?</span></span>
<span data-ttu-id="68b13-177">Eftirfarandi töflur sýna virknitákn og infix-tákn sem hægt er að nota þegar segðarskorða er skrifuð fyrir íhlut í afbrigðalíkani afurðar.</span><span class="sxs-lookup"><span data-stu-id="68b13-177">The following tables list the operators and infix notation that you can use when you write an expression constraint for a component in a product configuration model.</span></span> <span data-ttu-id="68b13-178">Í dæmunum hér í fyrri töflunni er hægt að sjá hvernig á að skrifa segð með því að nota annaðhvort infix-tákn eða virknitákn.</span><span class="sxs-lookup"><span data-stu-id="68b13-178">The examples in the first table show how to write an expression by using either infix notation or operators.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="68b13-179">Virknitákn</span><span class="sxs-lookup"><span data-stu-id="68b13-179">Operator</span></span></th>
<th><span data-ttu-id="68b13-180">Lýsing</span><span class="sxs-lookup"><span data-stu-id="68b13-180">Description</span></span></th>
<th><span data-ttu-id="68b13-181">Málskipun</span><span class="sxs-lookup"><span data-stu-id="68b13-181">Syntax</span></span></th>
<th><span data-ttu-id="68b13-182">Dæmi</span><span class="sxs-lookup"><span data-stu-id="68b13-182">Examples</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="68b13-183">Felur í sér</span><span class="sxs-lookup"><span data-stu-id="68b13-183">Implies</span></span></td>
<td><span data-ttu-id="68b13-184">Þetta er satt ef fyrsta skilyrðið er rangt, annað skilyrðið er rétt, eða bæði.</span><span class="sxs-lookup"><span data-stu-id="68b13-184">This is true if the first condition is false, the second condition is true, or both.</span></span></td>
<td><span data-ttu-id="68b13-185">Felur í sér [a, b], infix: a -: b</span><span class="sxs-lookup"><span data-stu-id="68b13-185">Implies[a, b], infix: a -: b</span></span></td>
<td><ul>
<li><span data-ttu-id="68b13-186"><strong>Operator:</strong> Bendir til[x != 0, y &gt;= 0]</span><span class="sxs-lookup"><span data-stu-id="68b13-186"><strong>Operator:</strong> Implies[x != 0, y &gt;= 0]</span></span></li>
<li><span data-ttu-id="68b13-187"><strong>Infix-tákn:</strong> x != 0 -: y &gt;= 0</span><span class="sxs-lookup"><span data-stu-id="68b13-187"><strong>Infix notation:</strong> x != 0 -: y &gt;= 0</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="68b13-188">Og</span><span class="sxs-lookup"><span data-stu-id="68b13-188">And</span></span></td>
<td><span data-ttu-id="68b13-189">Þetta er satt ef öll skilyrði eru uppfyllt.</span><span class="sxs-lookup"><span data-stu-id="68b13-189">This is true only if all conditions are true.</span></span> <span data-ttu-id="68b13-190">Ef skilyrði er 0 (núll), framleiðir það <strong>Rétt</strong>.</span><span class="sxs-lookup"><span data-stu-id="68b13-190">If the number of conditions is 0 (zero), it produces <strong>True</strong>.</span></span></td>
<td><span data-ttu-id="68b13-191">Og[args], infix: a &amp; b &amp; ... &amp; z</span><span class="sxs-lookup"><span data-stu-id="68b13-191">And[args], infix: a &amp; b &amp; ... &amp; z</span></span></td>
<td><ul>
<li><span data-ttu-id="68b13-192"><strong>Virknitákn:</strong> Og[x == 2, y &lt;= 2]</span><span class="sxs-lookup"><span data-stu-id="68b13-192"><strong>Operator:</strong> And[x == 2, y &lt;= 2]</span></span></li>
<li><span data-ttu-id="68b13-193"><strong>Infix-tákn:</strong> x == 2 &amp; y &lt;= 2</span><span class="sxs-lookup"><span data-stu-id="68b13-193"><strong>Infix notation:</strong> x == 2 &amp; y &lt;= 2</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="68b13-194">Eða</span><span class="sxs-lookup"><span data-stu-id="68b13-194">Or</span></span></td>
<td><span data-ttu-id="68b13-195">Þetta er satt ef hvaða skilyrði er satt.</span><span class="sxs-lookup"><span data-stu-id="68b13-195">This is true if any condition is true.</span></span> <span data-ttu-id="68b13-196">Ef skilyrði er 0 (núll), framleiðir það <strong>Rangt</strong>.</span><span class="sxs-lookup"><span data-stu-id="68b13-196">If the number of conditions is 0 (zero), it produces <strong>False</strong>.</span></span></td>
<td><span data-ttu-id="68b13-197">Eða[args], infix: a | b | ... | z</span><span class="sxs-lookup"><span data-stu-id="68b13-197">Or[args], infix: a | b | ... | z</span></span></td>
<td><ul>
<li><span data-ttu-id="68b13-198"><strong>Virknitákn:</strong> Or[x == 2, y &lt;= 2]</span><span class="sxs-lookup"><span data-stu-id="68b13-198"><strong>Operator:</strong> Or[x == 2, y &lt;= 2]</span></span></li>
<li><span data-ttu-id="68b13-199"><strong>Infix-tákn:</strong> x == 2 | y &lt;= 2</span><span class="sxs-lookup"><span data-stu-id="68b13-199"><strong>Infix notation:</strong> x == 2 | y &lt;= 2</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="68b13-200">Plús</span><span class="sxs-lookup"><span data-stu-id="68b13-200">Plus</span></span></td>
<td><span data-ttu-id="68b13-201">Þetta samtölur hennar skilyrði.</span><span class="sxs-lookup"><span data-stu-id="68b13-201">This sums its conditions.</span></span> <span data-ttu-id="68b13-202">Ef fjöldi skilyrða er 0 (núll), framleiðir það <strong>0</strong>.</span><span class="sxs-lookup"><span data-stu-id="68b13-202">If the number of conditions is 0 (zero), it produces <strong>0</strong>.</span></span></td>
<td><span data-ttu-id="68b13-203">Plús[args], infix: a + b + ... + z</span><span class="sxs-lookup"><span data-stu-id="68b13-203">Plus[args], infix: a + b + ... + z</span></span></td>
<td><ul>
<li><span data-ttu-id="68b13-204"><strong>Virknitákn:</strong> Plus[x, y, 2] == z</span><span class="sxs-lookup"><span data-stu-id="68b13-204"><strong>Operator:</strong> Plus[x, y, 2] == z</span></span></li>
<li><span data-ttu-id="68b13-205"><strong>Infix-tákn:</strong> x + y + 2 == z</span><span class="sxs-lookup"><span data-stu-id="68b13-205"><strong>Infix notation:</strong> x + y + 2 == z</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="68b13-206">Mínus</span><span class="sxs-lookup"><span data-stu-id="68b13-206">Minus</span></span></td>
<td><span data-ttu-id="68b13-207">Þetta negates hennar frumbreytu.</span><span class="sxs-lookup"><span data-stu-id="68b13-207">This negates its argument.</span></span> <span data-ttu-id="68b13-208">Þetta verður að hafa nákvæmlega eitt skilyrði.</span><span class="sxs-lookup"><span data-stu-id="68b13-208">It must have exactly one condition.</span></span></td>
<td><span data-ttu-id="68b13-209">Mínus [expr] infix: -expr</span><span class="sxs-lookup"><span data-stu-id="68b13-209">Minus[expr], infix: -expr</span></span></td>
<td><ul>
<li><span data-ttu-id="68b13-210"><strong>Virknitákn:</strong> Minus[x] == y</span><span class="sxs-lookup"><span data-stu-id="68b13-210"><strong>Operator:</strong> Minus[x] == y</span></span></li>
<li><span data-ttu-id="68b13-211"><strong>Infix-tákn:</strong> -x == y</span><span class="sxs-lookup"><span data-stu-id="68b13-211"><strong>Infix notation:</strong> -x == y</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="68b13-212">Abs</span><span class="sxs-lookup"><span data-stu-id="68b13-212">Abs</span></span></td>
<td><span data-ttu-id="68b13-213">Þetta tekur raungildi hennar skilyrði.</span><span class="sxs-lookup"><span data-stu-id="68b13-213">This takes the absolute value of its condition.</span></span> <span data-ttu-id="68b13-214">Þetta verður að hafa nákvæmlega eitt skilyrði.</span><span class="sxs-lookup"><span data-stu-id="68b13-214">It must have exactly one condition.</span></span></td>
<td><span data-ttu-id="68b13-215">[Expr] abs</span><span class="sxs-lookup"><span data-stu-id="68b13-215">Abs[expr]</span></span></td>
<td><span data-ttu-id="68b13-216"><strong>Virknitákn:</strong> Abs[x]</span><span class="sxs-lookup"><span data-stu-id="68b13-216"><strong>Operator:</strong> Abs[x]</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="68b13-217">Tímar</span><span class="sxs-lookup"><span data-stu-id="68b13-217">Times</span></span></td>
<td><span data-ttu-id="68b13-218">Þetta tekur afurðar þess skilyrða.</span><span class="sxs-lookup"><span data-stu-id="68b13-218">This takes the product of its conditions.</span></span> <span data-ttu-id="68b13-219">Ef fjöldi skilyrða er 0 (núll), framleiðir það <strong>1</strong>.</span><span class="sxs-lookup"><span data-stu-id="68b13-219">If the number of conditions is 0 (zero), it produces <strong>1</strong>.</span></span></td>
<td><span data-ttu-id="68b13-220">Sinnum[args], infix: a \* b \* ... \* z</span><span class="sxs-lookup"><span data-stu-id="68b13-220">Times[args], infix: a \* b \* ... \* z</span></span></td>
<td><ul>
<li><span data-ttu-id="68b13-221"><strong>Virknitákn:</strong> Times[x, y, 2] == z</span><span class="sxs-lookup"><span data-stu-id="68b13-221"><strong>Operator:</strong> Times[x, y, 2] == z</span></span></li>
<li><span data-ttu-id="68b13-222"><strong>Infix-tákn:</strong> x \* y \* 2 == z</span><span class="sxs-lookup"><span data-stu-id="68b13-222"><strong>Infix notation:</strong> x \* y \* 2 == z</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="68b13-223">Styrkur</span><span class="sxs-lookup"><span data-stu-id="68b13-223">Power</span></span></td>
<td><span data-ttu-id="68b13-224">Þetta tekur til exponential.</span><span class="sxs-lookup"><span data-stu-id="68b13-224">This takes an exponential.</span></span> <span data-ttu-id="68b13-225">Þetta á við veldi frá hægri til vinstri.</span><span class="sxs-lookup"><span data-stu-id="68b13-225">It applies exponentiation from right to left.</span></span> <span data-ttu-id="68b13-226">(Með öðrum orðum &#39; hægri-tengt.) Þess vegna er <strong>Power[a, b, c]</strong> jafnt og <strong>Power[a, Power[b, c]]</strong>.</span><span class="sxs-lookup"><span data-stu-id="68b13-226">(In other words, it&#39;s right-associative.) Therefore, <strong>Power[a, b, c]</strong> is equivalent to <strong>Power[a, Power[b, c]]</strong>.</span></span> <span data-ttu-id="68b13-227"><strong>Afl</strong> er aðeins hægt að nota með jákvæða fasta sem veldisvísi.</span><span class="sxs-lookup"><span data-stu-id="68b13-227"><strong>Power</strong> can be used only if the exponent is a positive constant.</span></span></td>
<td><span data-ttu-id="68b13-228">Power[args], infix: a ^ b ^ ... ^ z</span><span class="sxs-lookup"><span data-stu-id="68b13-228">Power[args], infix: a ^ b ^ ... ^ z</span></span></td>
<td><ul>
<li><span data-ttu-id="68b13-229"><strong>Virknitákn:</strong> Power[x, 2] == y</span><span class="sxs-lookup"><span data-stu-id="68b13-229"><strong>Operator:</strong> Power[x, 2] == y</span></span></li>
<li><span data-ttu-id="68b13-230"><strong>Infix-tákn:</strong> x ^ 2 == y</span><span class="sxs-lookup"><span data-stu-id="68b13-230"><strong>Infix notation:</strong> x ^ 2 == y</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="68b13-231">Hámark</span><span class="sxs-lookup"><span data-stu-id="68b13-231">Max</span></span></td>
<td><span data-ttu-id="68b13-232">Þetta myndar stærsta skilyrðið.</span><span class="sxs-lookup"><span data-stu-id="68b13-232">This produces the largest condition.</span></span> <span data-ttu-id="68b13-233">Ef fjöldi skilyrða er 0 (núll), framleiðir það <strong>Óendanleiki</strong>.</span><span class="sxs-lookup"><span data-stu-id="68b13-233">If the number of conditions is 0 (zero), it produces <strong>Infinity</strong>.</span></span></td>
<td><span data-ttu-id="68b13-234">Max [viðföng]</span><span class="sxs-lookup"><span data-stu-id="68b13-234">Max[args]</span></span></td>
<td><span data-ttu-id="68b13-235"><strong>Virknitákn:</strong> Max[x, y, 2] == z</span><span class="sxs-lookup"><span data-stu-id="68b13-235"><strong>Operator:</strong> Max[x, y, 2] == z</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="68b13-236">Lágmark</span><span class="sxs-lookup"><span data-stu-id="68b13-236">Min</span></span></td>
<td><span data-ttu-id="68b13-237">Þetta birtir lægstu skilyrði.</span><span class="sxs-lookup"><span data-stu-id="68b13-237">This produces the smallest condition.</span></span> <span data-ttu-id="68b13-238">Ef fjöldi skilyrða er 0 (núll), framleiðir það <strong>Óendanleiki</strong>.</span><span class="sxs-lookup"><span data-stu-id="68b13-238">If the number of conditions is 0 (zero), it produces <strong>Infinity</strong>.</span></span></td>
<td><span data-ttu-id="68b13-239">Mín. [viðföng]</span><span class="sxs-lookup"><span data-stu-id="68b13-239">Min[args]</span></span></td>
<td><span data-ttu-id="68b13-240"><strong>Virknitákn:</strong> Min[x, y, 2] == z</span><span class="sxs-lookup"><span data-stu-id="68b13-240"><strong>Operator:</strong> Min[x, y, 2] == z</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="68b13-241">Ekki</span><span class="sxs-lookup"><span data-stu-id="68b13-241">Not</span></span></td>
<td><span data-ttu-id="68b13-242">Þetta myndar röklegt inverse skilyrðis hennar.</span><span class="sxs-lookup"><span data-stu-id="68b13-242">This produces the logical inverse of its condition.</span></span> <span data-ttu-id="68b13-243">Þetta verður að hafa nákvæmlega eitt skilyrði.</span><span class="sxs-lookup"><span data-stu-id="68b13-243">It must have exactly one condition.</span></span></td>
<td><span data-ttu-id="68b13-244">Ekki [expr] infix: expr</span><span class="sxs-lookup"><span data-stu-id="68b13-244">Not[expr], infix: !expr</span></span></td>
<td><ul>
<li><span data-ttu-id="68b13-245"><strong>Virknitákn:</strong> Ekki[x] &amp; Ekki[y == 3]</span><span class="sxs-lookup"><span data-stu-id="68b13-245"><strong>Operator:</strong> Not[x] &amp; Not[y == 3]</span></span></li>
<li><span data-ttu-id="68b13-246"><strong>Infix-tákn:</strong> !x!(y == 3)</span><span class="sxs-lookup"><span data-stu-id="68b13-246"><strong>Infix notation:</strong> !x!(y == 3)</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

<span data-ttu-id="68b13-247">Dæmi í næstu töflu sýna hvernig á að skrifa infix-tákn.</span><span class="sxs-lookup"><span data-stu-id="68b13-247">The examples in the next table show how to write infix notation.</span></span>


|  <span data-ttu-id="68b13-248">Infix merki</span><span class="sxs-lookup"><span data-stu-id="68b13-248">Infix notation</span></span>   |                                          <span data-ttu-id="68b13-249">lýsing</span><span class="sxs-lookup"><span data-stu-id="68b13-249">Description</span></span>                                          |
|-------------------|-----------------------------------------------------------------------------------------------|
|     <span data-ttu-id="68b13-250">x + y + z</span><span class="sxs-lookup"><span data-stu-id="68b13-250">x + y + z</span></span>     |                                           <span data-ttu-id="68b13-251">samlagning</span><span class="sxs-lookup"><span data-stu-id="68b13-251">Addition</span></span>                                            |
|    <span data-ttu-id="68b13-252">x \* y \* z</span><span class="sxs-lookup"><span data-stu-id="68b13-252">x \* y \* z</span></span>    |                                        <span data-ttu-id="68b13-253">Margföldun</span><span class="sxs-lookup"><span data-stu-id="68b13-253">Multiplication</span></span>                                         |
|       <span data-ttu-id="68b13-254">x - y</span><span class="sxs-lookup"><span data-stu-id="68b13-254">x - y</span></span>       | <span data-ttu-id="68b13-255">Frádráttur tvíundakerfis er umreiknaður eins og viðbót tvíundakerfis þar sem er neitaða aðra.</span><span class="sxs-lookup"><span data-stu-id="68b13-255">Binary subtraction is translated the same as binary addition where there is a negated second.</span></span> |
|     <span data-ttu-id="68b13-256">x ^ y ^ z</span><span class="sxs-lookup"><span data-stu-id="68b13-256">x ^ y ^ z</span></span>     |                          <span data-ttu-id="68b13-257">Veldi sem hefur hægri tengslavirkni</span><span class="sxs-lookup"><span data-stu-id="68b13-257">Exponentiation that has right associativity</span></span>                          |
|        <span data-ttu-id="68b13-258">!x</span><span class="sxs-lookup"><span data-stu-id="68b13-258">!x</span></span>         |                                          <span data-ttu-id="68b13-259">Boole-ekki</span><span class="sxs-lookup"><span data-stu-id="68b13-259">Boolean not</span></span>                                          |
|      <span data-ttu-id="68b13-260">x -: y</span><span class="sxs-lookup"><span data-stu-id="68b13-260">x -: y</span></span>       |                                      <span data-ttu-id="68b13-261">Boole-leiðing</span><span class="sxs-lookup"><span data-stu-id="68b13-261">Boolean implication</span></span>                                      |
|         <span data-ttu-id="68b13-262">x</span><span class="sxs-lookup"><span data-stu-id="68b13-262">x</span></span>         |                                               <span data-ttu-id="68b13-263">y</span><span class="sxs-lookup"><span data-stu-id="68b13-263">y</span></span>                                               |
|     <span data-ttu-id="68b13-264">x & y & z</span><span class="sxs-lookup"><span data-stu-id="68b13-264">x & y & z</span></span>     |                                          <span data-ttu-id="68b13-265">Boole- og</span><span class="sxs-lookup"><span data-stu-id="68b13-265">Boolean and</span></span>                                          |
|    <span data-ttu-id="68b13-266">x == y == z</span><span class="sxs-lookup"><span data-stu-id="68b13-266">x == y == z</span></span>    |                                           <span data-ttu-id="68b13-267">Jafngildi</span><span class="sxs-lookup"><span data-stu-id="68b13-267">Equality</span></span>                                            |
|    <span data-ttu-id="68b13-268">x != y != z</span><span class="sxs-lookup"><span data-stu-id="68b13-268">x != y != z</span></span>    |                                           <span data-ttu-id="68b13-269">Ákveðið</span><span class="sxs-lookup"><span data-stu-id="68b13-269">Distinct</span></span>                                            |
|  <span data-ttu-id="68b13-270">x &lt; y &lt; z</span><span class="sxs-lookup"><span data-stu-id="68b13-270">x &lt; y &lt; z</span></span>  |                                           <span data-ttu-id="68b13-271">Minna en</span><span class="sxs-lookup"><span data-stu-id="68b13-271">Less than</span></span>                                           |
|  <span data-ttu-id="68b13-272">x &gt; y &gt; z</span><span class="sxs-lookup"><span data-stu-id="68b13-272">x &gt; y &gt; z</span></span>  |                                         <span data-ttu-id="68b13-273">Stærra en</span><span class="sxs-lookup"><span data-stu-id="68b13-273">Greater than</span></span>                                          |
| <span data-ttu-id="68b13-274">x &lt;= y &lt;= z</span><span class="sxs-lookup"><span data-stu-id="68b13-274">x &lt;= y &lt;= z</span></span> |                                     <span data-ttu-id="68b13-275">Minna en eða jafnt og</span><span class="sxs-lookup"><span data-stu-id="68b13-275">Less than or equal to</span></span>                                     |
| <span data-ttu-id="68b13-276">x &gt;= y &gt;= z</span><span class="sxs-lookup"><span data-stu-id="68b13-276">x &gt;= y &gt;= z</span></span> |                                   <span data-ttu-id="68b13-277">Stærra en eða jafnt og</span><span class="sxs-lookup"><span data-stu-id="68b13-277">Greater than or equal to</span></span>                                    |
|        <span data-ttu-id="68b13-278">(x)</span><span class="sxs-lookup"><span data-stu-id="68b13-278">(x)</span></span>        |                           <span data-ttu-id="68b13-279">Svigaar hnekkja sjálfgefinn forgang.</span><span class="sxs-lookup"><span data-stu-id="68b13-279">Parentheses override default precedence.</span></span>                            |

## <a name="why-arent-my-expression-constraints-validated-correctly"></a><span data-ttu-id="68b13-280">Af hverju eru mínar segðaskorður ekki sannprófaðar rétt?</span><span class="sxs-lookup"><span data-stu-id="68b13-280">Why aren't my expression constraints validated correctly?</span></span>
<span data-ttu-id="68b13-281">Frátekið lykilorð er hægt að nota sem heiti leysara eigindir, íhluti eða undiríhlutir í afbrigðalíkani afurðar.</span><span class="sxs-lookup"><span data-stu-id="68b13-281">You can't use reserved keywords as solver names for attributes, components, or subcomponents in a product configuration model.</span></span> <span data-ttu-id="68b13-282">Hér er listi yfir frátekin lykilorð sem ekki er hægt að nota:</span><span class="sxs-lookup"><span data-stu-id="68b13-282">Here is a list of the reserved keywords that you can't use:</span></span>

-   <span data-ttu-id="68b13-283">Þak</span><span class="sxs-lookup"><span data-stu-id="68b13-283">Ceiling</span></span>
-   <span data-ttu-id="68b13-284">Eining</span><span class="sxs-lookup"><span data-stu-id="68b13-284">Element</span></span>
-   <span data-ttu-id="68b13-285">Jafnt</span><span class="sxs-lookup"><span data-stu-id="68b13-285">Equal</span></span>
-   <span data-ttu-id="68b13-286">Hæð</span><span class="sxs-lookup"><span data-stu-id="68b13-286">Floor</span></span>
-   <span data-ttu-id="68b13-287">Ef</span><span class="sxs-lookup"><span data-stu-id="68b13-287">If</span></span>
-   <span data-ttu-id="68b13-288">Minna</span><span class="sxs-lookup"><span data-stu-id="68b13-288">Less</span></span>
-   <span data-ttu-id="68b13-289">Hærri</span><span class="sxs-lookup"><span data-stu-id="68b13-289">Greater</span></span>
-   <span data-ttu-id="68b13-290">Felur í sér</span><span class="sxs-lookup"><span data-stu-id="68b13-290">Implies</span></span>
-   <span data-ttu-id="68b13-291">Kladdi</span><span class="sxs-lookup"><span data-stu-id="68b13-291">Log</span></span>
-   <span data-ttu-id="68b13-292">Hám.</span><span class="sxs-lookup"><span data-stu-id="68b13-292">Max</span></span>
-   <span data-ttu-id="68b13-293">Mín.</span><span class="sxs-lookup"><span data-stu-id="68b13-293">Min</span></span>
-   <span data-ttu-id="68b13-294">Mínus</span><span class="sxs-lookup"><span data-stu-id="68b13-294">Minus</span></span>
-   <span data-ttu-id="68b13-295">Plús</span><span class="sxs-lookup"><span data-stu-id="68b13-295">Plus</span></span>
-   <span data-ttu-id="68b13-296">Styrkur</span><span class="sxs-lookup"><span data-stu-id="68b13-296">Power</span></span>
-   <span data-ttu-id="68b13-297">Tímar</span><span class="sxs-lookup"><span data-stu-id="68b13-297">Times</span></span>
-   <span data-ttu-id="68b13-298">Rauf</span><span class="sxs-lookup"><span data-stu-id="68b13-298">Slot</span></span>
-   <span data-ttu-id="68b13-299">Tegund</span><span class="sxs-lookup"><span data-stu-id="68b13-299">Model</span></span>
-   <span data-ttu-id="68b13-300">Ákvörðun</span><span class="sxs-lookup"><span data-stu-id="68b13-300">Decision</span></span>
-   <span data-ttu-id="68b13-301">Markmið</span><span class="sxs-lookup"><span data-stu-id="68b13-301">Goal</span></span>


<a name="additional-resources"></a><span data-ttu-id="68b13-302">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="68b13-302">Additional resources</span></span>
--------

[<span data-ttu-id="68b13-303">Stofna segð töfluskorðu</span><span class="sxs-lookup"><span data-stu-id="68b13-303">Create an expression constraint</span></span>](tasks/add-expression-constraint-product-configuration-model.md)

[<span data-ttu-id="68b13-304">Bæta útreikningi við afbrigðalíkan afurðar</span><span class="sxs-lookup"><span data-stu-id="68b13-304">Add a calculation to a product configuration model</span></span>](tasks/add-calculation-product-configuration-model.md)



