---
title: Ítarleg sía og málskipan fyrirspurna
description: Þetta efni lýsir síunar- og fyrirspurnarmöguleikum sem eru tiltækar þegar þú notar svargluggann fyrir sía/raða ítarlega eða samsvörun virknitáknið á síusvæðinu eða síur fyrir dálkhaus hnitanets.
author: jasongre
manager: AnnBe
ms.date: 03/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysQueryForm
audience: Application User
ms.reviewer: sericks
ms.custom: 3811
ms.assetid: b4969b30-2fe1-4a3c-bbea-725dc37c8b60
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b867099b131594a64cad102e50ead7c355594f2b
ms.sourcegitcommit: f5e31c34640add6d40308ac1365cc0ee60e60e24
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/08/2020
ms.locfileid: "4694544"
---
# <a name="advanced-filtering-and-query-syntax"></a><span data-ttu-id="3a4eb-103">Ítarleg sía og málskipan fyrirspurna</span><span class="sxs-lookup"><span data-stu-id="3a4eb-103">Advanced filtering and query syntax</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3a4eb-104">Þetta efni lýsir síunar- og fyrirspurnarmöguleikum sem eru tiltækar þegar þú notar svargluggann fyrir sía/raða ítarlega eða **samsvörunar**-virknitáknið á síusvæðinu eða síur fyrir dálkhaus hnitanets.</span><span class="sxs-lookup"><span data-stu-id="3a4eb-104">This topic describes the filtering and query options that are available when you use the Advanced filter/sort dialog or the **matches** operator in the Filter pane or grid column header filters.</span></span>

## <a name="advanced-query-syntax"></a><span data-ttu-id="3a4eb-105">Ítarleg fyrirspurnarmálskipan</span><span class="sxs-lookup"><span data-stu-id="3a4eb-105">Advanced query syntax</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="3a4eb-106">Málskipun</span><span class="sxs-lookup"><span data-stu-id="3a4eb-106">Syntax</span></span></th>
<th><span data-ttu-id="3a4eb-107">Lýsing á tákni</span><span class="sxs-lookup"><span data-stu-id="3a4eb-107">Character description</span></span></th>
<th><span data-ttu-id="3a4eb-108">lýsing</span><span class="sxs-lookup"><span data-stu-id="3a4eb-108">Description</span></span></th>
<th><span data-ttu-id="3a4eb-109">Dæmi</span><span class="sxs-lookup"><span data-stu-id="3a4eb-109">Example</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="3a4eb-110"><em>gildi</em></span><span class="sxs-lookup"><span data-stu-id="3a4eb-110"><em>value</em></span></span></td>
<td><span data-ttu-id="3a4eb-111">jafnt og gildið sem fært var inn.</span><span class="sxs-lookup"><span data-stu-id="3a4eb-111">Equal to the value that is entered</span></span></td>
<td><span data-ttu-id="3a4eb-112">Sláið inn gildi til að finna.</span><span class="sxs-lookup"><span data-stu-id="3a4eb-112">Type the value to find.</span></span></td>
<td><span data-ttu-id="3a4eb-113"><strong>Smith</strong> finnur &quot;Smith&quot;.</span><span class="sxs-lookup"><span data-stu-id="3a4eb-113"><strong>Smith</strong> finds &quot;Smith&quot;.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3a4eb-114">!<em>-gildi</em> (upphrópunarmerki)</span><span class="sxs-lookup"><span data-stu-id="3a4eb-114">!<em>value</em> (exclamation point)</span></span></td>
<td><span data-ttu-id="3a4eb-115">Ekki jafnt og gildið sem fært var inn.</span><span class="sxs-lookup"><span data-stu-id="3a4eb-115">Not equal to the value that is entered</span></span></td>
<td><span data-ttu-id="3a4eb-116">Færðu inn upphrópunarmerki og síðan gildið til að undanskilja.</span><span class="sxs-lookup"><span data-stu-id="3a4eb-116">Type an exclamation point and then the value to exclude.</span></span></td>
<td><span data-ttu-id="3a4eb-117"><strong>!Smith</strong> finnur öll gildi nema &quot;Smith&quot;.</span><span class="sxs-lookup"><span data-stu-id="3a4eb-117"><strong>!Smith</strong> finds all values except &quot;Smith&quot;.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3a4eb-118"><em>frá-gildi</em>..<em>til- gildi</em> (tvöfaldur punktur)</span><span class="sxs-lookup"><span data-stu-id="3a4eb-118"><em>from-value</em>..<em>to-value</em> (double period)</span></span></td>
<td><span data-ttu-id="3a4eb-119">Á milli tveggja gilda sem eru inn aðskilin með tveimur punktum.</span><span class="sxs-lookup"><span data-stu-id="3a4eb-119">Between the two values that are separated by double periods</span></span></td>
<td><span data-ttu-id="3a4eb-120">Færa inn Frá gildið, færa svo inn tvo punkta og síðan Til gildið.</span><span class="sxs-lookup"><span data-stu-id="3a4eb-120">Type the from-value, then two periods, and then the to-value.</span></span></td>
<td><span data-ttu-id="3a4eb-121"><strong>1..10</strong> finnur öll gildi frá 1 til og með 10.</span><span class="sxs-lookup"><span data-stu-id="3a4eb-121"><strong>1..10</strong> finds all values from 1 through 10.</span></span> <span data-ttu-id="3a4eb-122">Á strengjasvæði finnur <strong>A..C</strong> aftur á móti öll gildi sem byrja á &quot;A&quot; og &quot;B&quot;, og gildi sem eru alveg jöfn &quot;C&quot;.</span><span class="sxs-lookup"><span data-stu-id="3a4eb-122">However, in a string field, <strong>A..C</strong> finds all values that start with &quot;A&quot; and &quot;B&quot;, and values that are exactly equal to &quot;C&quot;.</span></span> <span data-ttu-id="3a4eb-123">Til dæmis finnur þessi fyrirspurn ekki &quot;Ca&quot;.</span><span class="sxs-lookup"><span data-stu-id="3a4eb-123">For example, this query won't find &quot;Ca&quot;.</span></span> <span data-ttu-id="3a4eb-124">Til að finna öll gildi frá &quot;A<em>&quot; til &quot;C</em>&quot;, færðu inn <strong>A..D</strong>.</span><span class="sxs-lookup"><span data-stu-id="3a4eb-124">To find all values from &quot;A<em>&quot; through &quot;C</em>&quot;, type <strong>A..D</strong>.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3a4eb-125"><em>gildi</em> (tvöfaldur punktur)</span><span class="sxs-lookup"><span data-stu-id="3a4eb-125">..<em>value</em> (double period)</span></span></td>
<td><span data-ttu-id="3a4eb-126">Minna en eða jafnt og gildið sem fært er inn.</span><span class="sxs-lookup"><span data-stu-id="3a4eb-126">Less than or equal to the value that is entered</span></span></td>
<td><span data-ttu-id="3a4eb-127">Færa inn tvo punkta og síðan gildið.</span><span class="sxs-lookup"><span data-stu-id="3a4eb-127">Type two periods and then the value.</span></span></td>
<td><span data-ttu-id="3a4eb-128"><strong>..1000</strong> finnur allar tölur sem eru minni en eða jafnar og 1000, t.d. &quot;100&quot;, &quot;999,95&quot; og &quot;1.000&quot;.</span><span class="sxs-lookup"><span data-stu-id="3a4eb-128"><strong>..1000</strong> finds any number that is less than or equal to 1000, such as &quot;100&quot;, &quot;999.95&quot;, and &quot;1,000&quot;.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3a4eb-129"><em>gildi</em>..</span><span class="sxs-lookup"><span data-stu-id="3a4eb-129"><em>value</em>..</span></span> <span data-ttu-id="3a4eb-130">(tveir punktar)</span><span class="sxs-lookup"><span data-stu-id="3a4eb-130">(double period)</span></span></td>
<td><span data-ttu-id="3a4eb-131">Meira en eða jafnt og gildið sem fært er inn.</span><span class="sxs-lookup"><span data-stu-id="3a4eb-131">Greater than or equal to the value that is entered</span></span></td>
<td><span data-ttu-id="3a4eb-132">Færa inn gildi og síðan tvo punkta.</span><span class="sxs-lookup"><span data-stu-id="3a4eb-132">Type the value and then two periods.</span></span></td>
<td><span data-ttu-id="3a4eb-133"><strong>1000 ..</strong></span><span class="sxs-lookup"><span data-stu-id="3a4eb-133"><strong>1000..</strong></span></span> <span data-ttu-id="3a4eb-134">1000.. finnur allar tölur sem eru meiri en eða jafnt og 1000, eins og &quot;1,000&quot;, &quot;1,000.01&quot;, og &quot;1,000,000&quot;.</span><span class="sxs-lookup"><span data-stu-id="3a4eb-134">finds any number that is greater than or equal to 1000, such as &quot;1,000&quot;, &quot;1,000.01&quot;, and &quot;1,000,000&quot;.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3a4eb-135">&gt;<em>gildi</em> (stærra en merki)</span><span class="sxs-lookup"><span data-stu-id="3a4eb-135">&gt;<em>value</em> (greater than sign)</span></span></td>
<td><span data-ttu-id="3a4eb-136">Stærra en gildið sem fært er inn.</span><span class="sxs-lookup"><span data-stu-id="3a4eb-136">Greater than the value that is entered</span></span></td>
<td><span data-ttu-id="3a4eb-137">Færðu inn stærra en-merki (<strong>&gt;</strong>) og síðan gildið.</span><span class="sxs-lookup"><span data-stu-id="3a4eb-137">Type a greater than sign (<strong>&gt;</strong>) and then the value.</span></span></td>
<td><span data-ttu-id="3a4eb-138"><strong>&gt;1000</strong> finnur allar tölur sem eru meiri en 1000, eins og &quot;1000.01&quot;, &quot;20,000&quot;, og &quot;1,000,000&quot;.</span><span class="sxs-lookup"><span data-stu-id="3a4eb-138"><strong>&gt;1000</strong> finds any number that is greater than 1000, such as &quot;1000.01&quot;, &quot;20,000&quot;, and &quot;1,000,000&quot;.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3a4eb-139">&lt;<em>gildi</em> (minna en merki)</span><span class="sxs-lookup"><span data-stu-id="3a4eb-139">&lt;<em>value</em> (less than sign)</span></span></td>
<td><span data-ttu-id="3a4eb-140">Minna en gildið sem fært er inn.</span><span class="sxs-lookup"><span data-stu-id="3a4eb-140">Less than the value that is entered</span></span></td>
<td><span data-ttu-id="3a4eb-141">Færðu inn minna en-merki (<strong>&lt;</strong>) og síðan gildið.</span><span class="sxs-lookup"><span data-stu-id="3a4eb-141">Type a less than sign (<strong>&lt;</strong>) and then the value.</span></span></td>
<td><span data-ttu-id="3a4eb-142"><strong>&lt;1000</strong> finnur allar tölur sem eru minni en 1000, eins og &quot;999.99&quot;, &quot;1&quot;, og &quot;-200&quot;.</span><span class="sxs-lookup"><span data-stu-id="3a4eb-142"><strong>&lt;1000</strong> finds any number that is less than 1000, such as &quot;999.99&quot;, &quot;1&quot;, and &quot;-200&quot;.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3a4eb-143"><em>gildi</em>\* (stjarna)</span><span class="sxs-lookup"><span data-stu-id="3a4eb-143"><em>value</em>\* (asterisk)</span></span></td>
<td><span data-ttu-id="3a4eb-144">Byrjar frá gildið sem fært er inn.</span><span class="sxs-lookup"><span data-stu-id="3a4eb-144">Starting from the value that is entered</span></span></td>
<td><span data-ttu-id="3a4eb-145">Færa inn upphafsgildið og síðan stjörnuna (<strong>\*</strong>)</span><span class="sxs-lookup"><span data-stu-id="3a4eb-145">Type the starting value and then an asterisk (<strong>\*</strong>).</span></span></td>
<td><span data-ttu-id="3a4eb-146"><strong>S\*</strong> finnur alla strengi sem byrja á &quot;S&quot;, eins og &quot;Stokkhólmur&quot;, &quot;Sydney&quot; og &quot;San Francisco&quot;.</span><span class="sxs-lookup"><span data-stu-id="3a4eb-146"><strong>S\*</strong> finds any string that starts with &quot;S&quot;, such as &quot;Stockholm&quot;, &quot;Sydney&quot;, and &quot;San Francisco&quot;.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3a4eb-147">\*<em>gildi</em> (stjarna)</span><span class="sxs-lookup"><span data-stu-id="3a4eb-147">\*<em>value</em> (asterisk)</span></span></td>
<td><span data-ttu-id="3a4eb-148">Endar á gildið sem fært er inn.</span><span class="sxs-lookup"><span data-stu-id="3a4eb-148">Ending with the value that is entered</span></span></td>
<td><span data-ttu-id="3a4eb-149">Færa inn stjörnu og síðan endagildið.</span><span class="sxs-lookup"><span data-stu-id="3a4eb-149">Type an asterisk and then the ending value.</span></span></td>
<td><span data-ttu-id="3a4eb-150"><strong>\*austur</strong> finnur alla strengi sem enda á &quot;austur&quot;, eins og &quot;Norðaustur&quot; og &quot;Suðaustur&quot;.</span><span class="sxs-lookup"><span data-stu-id="3a4eb-150"><strong>\*east</strong> finds any string that ends with &quot;east&quot;, such as &quot;Northeast&quot; and &quot;Southeast&quot;.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3a4eb-151">*<em>gildi</em>* (stjarna)</span><span class="sxs-lookup"><span data-stu-id="3a4eb-151">*<em>value</em>* (asterisk)</span></span></td>
<td><span data-ttu-id="3a4eb-152">Inniheldur gildið sem fært er inn.</span><span class="sxs-lookup"><span data-stu-id="3a4eb-152">Containing the value that is entered</span></span></td>
<td><span data-ttu-id="3a4eb-153">Færa inn stjörnu, gildi og síðan aðra stjörnu.</span><span class="sxs-lookup"><span data-stu-id="3a4eb-153">Type an asterisk, then a value, and then another asterisk.</span></span></td>
<td><span data-ttu-id="3a4eb-154"><strong>*rð*</strong> finnur alla strengi sem innihalda &quot;rð&quot;, eins og &quot;Norðaustur&quot; og &quot;Suðaustur&quot;.</span><span class="sxs-lookup"><span data-stu-id="3a4eb-154"><strong>*th*</strong> finds any string that contains &quot;th&quot;, such as &quot;Northeast&quot; and &quot;Southeast&quot;.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3a4eb-155">?</span><span class="sxs-lookup"><span data-stu-id="3a4eb-155">?</span></span> <span data-ttu-id="3a4eb-156">(spurningamerki)</span><span class="sxs-lookup"><span data-stu-id="3a4eb-156">(question mark)</span></span></td>
<td><span data-ttu-id="3a4eb-157">Innihalda einn eða fleiri óþekkta stafi</span><span class="sxs-lookup"><span data-stu-id="3a4eb-157">Having one or more unknown characters</span></span></td>
<td><span data-ttu-id="3a4eb-158">Færðu inn spurningamerki við stöðu óþekkts staftákns í gildinu.</span><span class="sxs-lookup"><span data-stu-id="3a4eb-158">Type a question mark at the position of the unknown character in the value.</span></span></td>
<td><span data-ttu-id="3a4eb-159"><strong>Sm?th</strong> finnur &quot;Smith&quot; og &quot;Smyth&quot;.</span><span class="sxs-lookup"><span data-stu-id="3a4eb-159"><strong>Sm?th</strong> finds &quot;Smith&quot; and &quot;Smyth&quot;.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3a4eb-160"><em>gildi</em>,<em>gildi</em> (komma)</span><span class="sxs-lookup"><span data-stu-id="3a4eb-160"><em>value</em>,<em>value</em> (comma)</span></span></td>
<td><span data-ttu-id="3a4eb-161">Samsvarar gildunum sem eru aðskilin með kommum.</span><span class="sxs-lookup"><span data-stu-id="3a4eb-161">Matching the values that are separated by commas</span></span></td>
<td><span data-ttu-id="3a4eb-162">Færa inn öll þín skilyrði, og aðskiljið þau með kommu.</span><span class="sxs-lookup"><span data-stu-id="3a4eb-162">Type all your criteria, and separate them by using commas.</span></span></td>
<td><span data-ttu-id="3a4eb-163"><strong>A, D, F, G</strong> finnur nákvæmlega &quot;A&quot;, &quot;D&quot;, &quot;F&quot;, og &quot;G&quot;.</span><span class="sxs-lookup"><span data-stu-id="3a4eb-163"><strong>A, D, F, G</strong> finds exactly &quot;A&quot;, &quot;D&quot;, &quot;F&quot;, and &quot;G&quot;.</span></span> <span data-ttu-id="3a4eb-164"><strong>10, 20, 30, 100</strong> finnur nákvæmlega &quot;10, 20, 30, 100&quot;.</span><span class="sxs-lookup"><span data-stu-id="3a4eb-164"><strong>10, 20, 30, 100</strong> finds exactly &quot;10, 20, 30, 100&quot;.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3a4eb-165">"" (tvær tvöföldar tilvitnanir)</span><span class="sxs-lookup"><span data-stu-id="3a4eb-165">"" (two double quotes)</span></span></td>
<td><span data-ttu-id="3a4eb-166">Samsvarar auðu gildi</span><span class="sxs-lookup"><span data-stu-id="3a4eb-166">Matching a blank value</span></span></td>
<td><span data-ttu-id="3a4eb-167">Sláðu inn tvær tvöfaldar tilvitnanir í röð til að sía fyrir auð gildi í þeim reit.</span><span class="sxs-lookup"><span data-stu-id="3a4eb-167">Type two consecutive double quotes to filter for blank values in that field.</span></span></td>
<td><span data-ttu-id="3a4eb-168">Tvær tvöföldar tilvitnanir í röð (<strong>""</strong>) finna línur án gildis fyrir núverandi dálk.</span><span class="sxs-lookup"><span data-stu-id="3a4eb-168">Two consecutive double quotes (<strong>""</strong>) finds rows with no value for the current column.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3a4eb-169">(<span class="code">Finance and Operations fyrirspurn</span>) (Finance and Operations fyrirspurn milli sviga)</span><span class="sxs-lookup"><span data-stu-id="3a4eb-169">(<span class="code">Finance and Operations query</span>) (Finance and Operations query between parentheses)</span></span></td>
<td><span data-ttu-id="3a4eb-170">Samsvarar tilgreindri fyrirspurn</span><span class="sxs-lookup"><span data-stu-id="3a4eb-170">Matching a defined query</span></span></td>
<td><span data-ttu-id="3a4eb-171">Sláðu inn fyrirspurn sem SQL staðhæfingu milli sviga með því að nota Finance and Operations fyrirspurnarmál.</span><span class="sxs-lookup"><span data-stu-id="3a4eb-171">Type a query as an SQL statement between parentheses using the Finance and Operations query language.</span></span></td>
  <td><span data-ttu-id="3a4eb-172"><strong><span class="code">((AccountNum LIKE "US *") && (DirPartyTable.Name LIKE "Cont*"))</span></strong></span><span class="sxs-lookup"><span data-stu-id="3a4eb-172"><strong><span class="code">((AccountNum LIKE "US *") && (DirPartyTable.Name LIKE "Cont*"))</span></strong></span></span><br><br> 
       <span data-ttu-id="3a4eb-173">Sem dæmi um málskipan fyrir síuaðstæður á reit frá gagnagrunni rótarinnar sem og reit frá öðrum gagnagrunna (fyrir síðuna Allir viðskiptavinir)</span><span class="sxs-lookup"><span data-stu-id="3a4eb-173">as an example of syntax for a filter condition on a field from the root datasource as well as a field from a different datasource (for the All customers page)</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3a4eb-174">Þ</span><span class="sxs-lookup"><span data-stu-id="3a4eb-174">T</span></span></td>
<td><span data-ttu-id="3a4eb-175">Dagurinn í dag</span><span class="sxs-lookup"><span data-stu-id="3a4eb-175">Today's date</span></span></td>
<td><span data-ttu-id="3a4eb-176">gerð <strong>T</strong>.</span><span class="sxs-lookup"><span data-stu-id="3a4eb-176">Type <strong>T</strong>.</span></span></td>
<td><span data-ttu-id="3a4eb-177"><strong>T</strong> samsvarar dagurinn í dag.</span><span class="sxs-lookup"><span data-stu-id="3a4eb-177"><strong>T</strong> matches today's date.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3a4eb-178">(methodName(parameters)) (<strong>SysQueryRangeUtil</strong> aðferð á milli sviga)</span><span class="sxs-lookup"><span data-stu-id="3a4eb-178">(methodName(parameters)) (<strong>SysQueryRangeUtil</strong> method between parentheses)</span></span></td>
<td><span data-ttu-id="3a4eb-179">Jöfnun gilda eða bil gilda sem eru tilgreind í færibreytum <strong>SysQueryRangeUtil</strong> aðferð</span><span class="sxs-lookup"><span data-stu-id="3a4eb-179">Matching the value or range of values that are specified by the parameters of the <strong>SysQueryRangeUtil</strong> method</span></span></td>
<td><span data-ttu-id="3a4eb-180">Færðu inn <strong>SysQueryRangeUtil</strong> aðferð sem er með færibreytum sem tilgreina gildi eða svið gilda.</span><span class="sxs-lookup"><span data-stu-id="3a4eb-180">Type a <strong>SysQueryRangeUtil</strong> method that has parameters that specify the value or range of values.</span></span></td>
<td>
<ol>
<li><span data-ttu-id="3a4eb-181">Smellt er á <strong>Viðskiptakröfur</strong> &gt; <strong>Reikningar</strong> &gt; <strong>Opið reikning viðskiptavinar</strong>.</span><span class="sxs-lookup"><span data-stu-id="3a4eb-181">Click <strong>Accounts receivable</strong> &gt; <strong>Invoices</strong> &gt; <strong>Open customer invoices</strong>.</span></span></li>
<li><span data-ttu-id="3a4eb-182">Styðjið á Ctrl + Shift + F3 til að opna í <strong>Fyrirspurn</strong> síðu.</span><span class="sxs-lookup"><span data-stu-id="3a4eb-182">Press Ctrl+Shift+F3 to open the <strong>Inquiry</strong> page.</span></span></li>
<li><span data-ttu-id="3a4eb-183">Á flipanum <strong>svið</strong>, er smellt á <strong>Bæta við</strong>.</span><span class="sxs-lookup"><span data-stu-id="3a4eb-183">On the <strong>Range</strong> tab, click <strong>Add</strong>.</span></span></li>
<li><span data-ttu-id="3a4eb-184">Í <strong>töflu</strong> reit, velja <strong>opnar færsla viðskiptavinar</strong>.</span><span class="sxs-lookup"><span data-stu-id="3a4eb-184">In the <strong>Table</strong> field, select <strong>Open customer transactions</strong>.</span></span></li>
<li><span data-ttu-id="3a4eb-185">Á svæðinu <strong>reitur</strong> velja <strong>gjalddagi</strong></span><span class="sxs-lookup"><span data-stu-id="3a4eb-185">In the <strong>Field</strong> field, select <strong>Due date</strong>.</span></span></li>
<li><span data-ttu-id="3a4eb-186">Í <strong>skilyrði</strong> reitnum, færa inn <strong>(yearRange(-2,0))</strong>.</span><span class="sxs-lookup"><span data-stu-id="3a4eb-186">In the <strong>Criteria</strong> field, enter <strong>(yearRange(-2,0))</strong>.</span></span></li>
<li><span data-ttu-id="3a4eb-187">Smelltu á <strong>Í lagi</strong>.</span><span class="sxs-lookup"><span data-stu-id="3a4eb-187">Click <strong>OK</strong>.</span></span> <span data-ttu-id="3a4eb-188">listasíða er uppfærð til að birta lista yfir reikninga sem stemma við skilyrði sem þú færðir inn.</span><span class="sxs-lookup"><span data-stu-id="3a4eb-188">The list page is updated and lists the invoices that match the criterion that you entered.</span></span> <span data-ttu-id="3a4eb-189">Í þessu dæmi eru reikningar sem voru á gjalddaga síðustu tvö ár taldir upp.</span><span class="sxs-lookup"><span data-stu-id="3a4eb-189">For this example, invoices that were due in the previous two years are listed.</span></span></li>
</ol>
<span data-ttu-id="3a4eb-190">Sjá töfluna í næsta hluta fyrir frekari upplýsingar um <strong>SysQueryRangeUtil</strong> dagsetningaraðferðir og nokkur dæmi.</span><span class="sxs-lookup"><span data-stu-id="3a4eb-190">See the table in the next section for additional details about <strong>SysQueryRangeUtil</strong> date methods, and several examples.</span></span></td>
</tr>
</tbody>
</table>

## <a name="advanced-date-queries-that-use-sysqueryrangeutil-methods"></a><span data-ttu-id="3a4eb-191">ítarlega dagsetningarfyrirspurnir sem nota SysQueryRangeUtil aðferðir</span><span class="sxs-lookup"><span data-stu-id="3a4eb-191">Advanced date queries that use SysQueryRangeUtil methods</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="3a4eb-192">Aðferð</span><span class="sxs-lookup"><span data-stu-id="3a4eb-192">Method</span></span></th>
<th><span data-ttu-id="3a4eb-193">Lýsing</span><span class="sxs-lookup"><span data-stu-id="3a4eb-193">Description</span></span></th>
<th><span data-ttu-id="3a4eb-194">Dæmi</span><span class="sxs-lookup"><span data-stu-id="3a4eb-194">Example</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="3a4eb-195">Dagur (_relativeDays=0)</span><span class="sxs-lookup"><span data-stu-id="3a4eb-195">Day (_relativeDays=0)</span></span></td>
<td><span data-ttu-id="3a4eb-196">Finna dagsetningu miðað við dagsetningu setu.</span><span class="sxs-lookup"><span data-stu-id="3a4eb-196">Find a date relative to the session date.</span></span> <span data-ttu-id="3a4eb-197">Jákvæð gildi tilgreina framtíðardagsetningar, og neikvæð gildi tilgreina liðnar dagsetningar.</span><span class="sxs-lookup"><span data-stu-id="3a4eb-197">Positive values indicate future dates, and negative values indicate past dates.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="3a4eb-198"><strong>Á morgun</strong> – færðu inn <strong>(dagur(1))</strong>.</span><span class="sxs-lookup"><span data-stu-id="3a4eb-198"><strong>Tomorrow</strong> – Enter <strong>(Day(1))</strong>.</span></span></li>
<li><span data-ttu-id="3a4eb-199"><strong>Í dag</strong> – Færðu inn <strong>(dagur(0))</strong>.</span><span class="sxs-lookup"><span data-stu-id="3a4eb-199"><strong>Today</strong> – Enter <strong>(Day(0))</strong>.</span></span></li>
<li><span data-ttu-id="3a4eb-200"><strong>Í gær</strong> – færðu inn <strong>(dagur(-1))</strong>.</span><span class="sxs-lookup"><span data-stu-id="3a4eb-200"><strong>Yesterday</strong> – Enter <strong>(Day(-1))</strong>.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="3a4eb-201">DayRange (_relativeDaysFrom=0, _relativeDaysTo=0)</span><span class="sxs-lookup"><span data-stu-id="3a4eb-201">DayRange (_relativeDaysFrom=0, _relativeDaysTo=0)</span></span></td>
<td><span data-ttu-id="3a4eb-202">Finna dagsetningarsvið miðað við dagsetningu setu.</span><span class="sxs-lookup"><span data-stu-id="3a4eb-202">Find a range of dates relative to the session date.</span></span> <span data-ttu-id="3a4eb-203">Jákvæð gildi tilgreina framtíðardagsetningar, og neikvæð gildi tilgreina liðnar dagsetningar.</span><span class="sxs-lookup"><span data-stu-id="3a4eb-203">Positive values indicate future dates, and negative values indicate past dates.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="3a4eb-204"><strong>Síðustu 30 daga</strong> - Sláðu inn <strong>" (DayRange (-30,0))</strong></span><span class="sxs-lookup"><span data-stu-id="3a4eb-204"><strong>Last 30 days</strong> – Enter <strong>(DayRange(-30,0))</strong>.</span></span></li>
<li><span data-ttu-id="3a4eb-205"><strong>Fyrri 30 dagar og næstu 30 dagar</strong> – færið inn <strong>“(DayRange(-30,30))”</strong></span><span class="sxs-lookup"><span data-stu-id="3a4eb-205"><strong>Previous 30 days and next 30 days</strong> – Enter <strong>(DayRange(-30,30))</strong>.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="3a4eb-206">GreaterThanDate (_relativeDays=0) GreaterThanUtcDate (_relativeDays=0)</span><span class="sxs-lookup"><span data-stu-id="3a4eb-206">GreaterThanDate (_relativeDays=0) GreaterThanUtcDate (_relativeDays=0)</span></span></td>
<td><span data-ttu-id="3a4eb-207">Leita að öllum dagsetningum eftir tilgreinda afstæða dagsetningu.</span><span class="sxs-lookup"><span data-stu-id="3a4eb-207">Find all dates after the specified relative date.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="3a4eb-208"><strong>Meira en 30 dagar frá því núna</strong> – færið Inn <strong>(GreaterThanDate(30))</strong>.</span><span class="sxs-lookup"><span data-stu-id="3a4eb-208"><strong>More than 30 days from now</strong> – Enter <strong>(GreaterThanDate(30))</strong>.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="3a4eb-209">GreaterThanUtcNow ()</span><span class="sxs-lookup"><span data-stu-id="3a4eb-209">GreaterThanUtcNow ()</span></span></td>
<td><span data-ttu-id="3a4eb-210">Finna allar færslur dagsetningar/tíma eftir núverandi tíma.</span><span class="sxs-lookup"><span data-stu-id="3a4eb-210">Find all date/time entries after the current time.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="3a4eb-211"><strong>Allar framtíðar dagsetningar/tími</strong> – færið Inn <strong>(GreaterThanUtcNow())</strong>.</span><span class="sxs-lookup"><span data-stu-id="3a4eb-211"><strong>All future date/times</strong> – Enter <strong>(GreaterThanUtcNow())</strong>.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="3a4eb-212">LessThanDate (_relativeDays=0) LessThanUtcDate (_relativeDays=0)</span><span class="sxs-lookup"><span data-stu-id="3a4eb-212">LessThanDate (_relativeDays=0) LessThanUtcDate (_relativeDays=0)</span></span></td>
<td><span data-ttu-id="3a4eb-213">Leita að öllum dagsetningum fyrir tilgreinda afstæða dagsetningu.</span><span class="sxs-lookup"><span data-stu-id="3a4eb-213">Find all dates before the specified relative date.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="3a4eb-214"><strong>Minna en sjö dagar frá núna</strong> – færið Inn <strong>(LessThanDate(7))</strong>.</span><span class="sxs-lookup"><span data-stu-id="3a4eb-214"><strong>Less than seven days from now</strong> – Enter <strong>(LessThanDate(7))</strong>.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="3a4eb-215">LessThanUtcNow ()</span><span class="sxs-lookup"><span data-stu-id="3a4eb-215">LessThanUtcNow ()</span></span></td>
<td><span data-ttu-id="3a4eb-216">Finna allar færslur dagsetningar/tíma fyrir núverandi tíma.</span><span class="sxs-lookup"><span data-stu-id="3a4eb-216">Find all date/time entries before the current time.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="3a4eb-217"><strong>Allar liðnar dagsetningu/tíma</strong> – færið Inn <strong>(LessThanUtcNow())</strong>.</span><span class="sxs-lookup"><span data-stu-id="3a4eb-217"><strong>All past date/times</strong> – Enter <strong>(LessThanUtcNow())</strong>.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="3a4eb-218">MonthRange (_relativeFrom=0, _relativeTo=0)</span><span class="sxs-lookup"><span data-stu-id="3a4eb-218">MonthRange (_relativeFrom=0, _relativeTo=0)</span></span></td>
<td><span data-ttu-id="3a4eb-219">Finna svið dagsetninga samkvæmt mánaða samanborið við núverandi mánuð</span><span class="sxs-lookup"><span data-stu-id="3a4eb-219">Find a range of dates, based on months relative to the current month.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="3a4eb-220"><strong>Fyrri tveir mánuðir</strong> – færið Inn <strong>(MonthRange(-2,0))</strong>.</span><span class="sxs-lookup"><span data-stu-id="3a4eb-220"><strong>Previous two months</strong> – Enter <strong>(MonthRange(-2,0))</strong>.</span></span></li>
<li><span data-ttu-id="3a4eb-221"><strong>Næstu þrír mánuðir</strong> – færið Inn <strong>(MonthRange(0,3))</strong>.</span><span class="sxs-lookup"><span data-stu-id="3a4eb-221"><strong>Next three months</strong> – Enter <strong>(MonthRange(0,3))</strong>.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="3a4eb-222">YearRange (_relativeFrom=0, _relativeTo=0)</span><span class="sxs-lookup"><span data-stu-id="3a4eb-222">YearRange (_relativeFrom=0, _relativeTo=0)</span></span></td>
<td><span data-ttu-id="3a4eb-223">Finna svið dagsetninga samkvæmt árum samanborið við í núverandi ár.</span><span class="sxs-lookup"><span data-stu-id="3a4eb-223">Find a range of dates, based on years relative to the current year.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="3a4eb-224"><strong>Næsta árs</strong> – færið Inn <strong>(YearRange (0, 1))</strong>.</span><span class="sxs-lookup"><span data-stu-id="3a4eb-224"><strong>Next year</strong> – Enter <strong>(YearRange(0, 1))</strong>.</span></span></li>
<li><span data-ttu-id="3a4eb-225"><strong>Fyrra ár</strong> – Færið Inn <strong>(YearRange (-1,0))</strong>.</span><span class="sxs-lookup"><span data-stu-id="3a4eb-225"><strong>Previous year</strong> – Enter <strong>(YearRange(-1,0))</strong>.</span></span></li>
</ul>
</td>
</tr>
</tbody>
</table>
