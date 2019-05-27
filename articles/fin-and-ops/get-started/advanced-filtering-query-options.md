---
title: Ítarleg sía og málskipan fyrirspurna
description: Þessi grein lýsir síunar- og fyrirspurnarmöguleikum sem eru tiltækar þegar þú notar svargluggann fyrir sía/raða ítarlega eða samsvörun virknitáknið á síusvæðinu eða síur fyrir dálkhaus hnitanets.
author: jasongre
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysQueryForm
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 3811
ms.assetid: b4969b30-2fe1-4a3c-bbea-725dc37c8b60
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 01a508e97721099f92b9167dfdfa1b9669b9341c
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/15/2019
ms.locfileid: "1547009"
---
# <a name="advanced-filtering-and-query-syntax"></a><span data-ttu-id="4a7d9-103">Ítarleg sía og málskipan fyrirspurna</span><span class="sxs-lookup"><span data-stu-id="4a7d9-103">Advanced filtering and query syntax</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4a7d9-104">Þessi grein lýsir síunar- og fyrirspurnarmöguleikum sem eru tiltækar þegar þú notar svargluggann fyrir sía/raða ítarlega eða **samsvörun** virknitáknið á síusvæðinu eða síur fyrir dálkhaus hnitanets.</span><span class="sxs-lookup"><span data-stu-id="4a7d9-104">This article describes the filtering and query options that are available when you use the Advanced filter/sort dialog or the **matches** operator in the Filter pane or grid column header filters.</span></span>

## <a name="advanced-query-syntax"></a><span data-ttu-id="4a7d9-105">Ítarleg fyrirspurnarmálskipan</span><span class="sxs-lookup"><span data-stu-id="4a7d9-105">Advanced query syntax</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="4a7d9-106">Málskipun</span><span class="sxs-lookup"><span data-stu-id="4a7d9-106">Syntax</span></span></th>
<th><span data-ttu-id="4a7d9-107">Lýsing á tákni</span><span class="sxs-lookup"><span data-stu-id="4a7d9-107">Character description</span></span></th>
<th><span data-ttu-id="4a7d9-108">lýsing</span><span class="sxs-lookup"><span data-stu-id="4a7d9-108">Description</span></span></th>
<th><span data-ttu-id="4a7d9-109">Dæmi</span><span class="sxs-lookup"><span data-stu-id="4a7d9-109">Example</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4a7d9-110"><em>gildi</em></span><span class="sxs-lookup"><span data-stu-id="4a7d9-110"><em>value</em></span></span></td>
<td><span data-ttu-id="4a7d9-111">jafnt og gildið sem fært var inn.</span><span class="sxs-lookup"><span data-stu-id="4a7d9-111">Equal to the value that is entered</span></span></td>
<td><span data-ttu-id="4a7d9-112">Sláið inn gildi til að finna.</span><span class="sxs-lookup"><span data-stu-id="4a7d9-112">Type the value to find.</span></span></td>
<td><span data-ttu-id="4a7d9-113"><strong>Smith</strong> finnur &quot;Smith&quot;.</span><span class="sxs-lookup"><span data-stu-id="4a7d9-113"><strong>Smith</strong> finds &quot;Smith&quot;.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4a7d9-114">!<em>-gildi</em> (upphrópunarmerki)</span><span class="sxs-lookup"><span data-stu-id="4a7d9-114">!<em>value</em> (exclamation point)</span></span></td>
<td><span data-ttu-id="4a7d9-115">Ekki jafnt og gildið sem fært var inn.</span><span class="sxs-lookup"><span data-stu-id="4a7d9-115">Not equal to the value that is entered</span></span></td>
<td><span data-ttu-id="4a7d9-116">Færðu inn upphrópunarmerki og síðan gildið til að undanskilja.</span><span class="sxs-lookup"><span data-stu-id="4a7d9-116">Type an exclamation point and then the value to exclude.</span></span></td>
<td><span data-ttu-id="4a7d9-117"><strong>!Smith</strong> finnur öll gildi nema &quot;Smith&quot;.</span><span class="sxs-lookup"><span data-stu-id="4a7d9-117"><strong>!Smith</strong> finds all values except &quot;Smith&quot;.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4a7d9-118"><em>frá-gildi</em>..<em>til- gildi</em> (tvöfaldur punktur)</span><span class="sxs-lookup"><span data-stu-id="4a7d9-118"><em>from-value</em>..<em>to-value</em> (double period)</span></span></td>
<td><span data-ttu-id="4a7d9-119">Á milli tveggja gilda sem eru inn aðskilin með tveimur punktum.</span><span class="sxs-lookup"><span data-stu-id="4a7d9-119">Between the two values that are separated by double periods</span></span></td>
<td><span data-ttu-id="4a7d9-120">Færa inn Frá gildið, færa svo inn tvo punkta og síðan Til gildið.</span><span class="sxs-lookup"><span data-stu-id="4a7d9-120">Type the from-value, then two periods, and then the to-value.</span></span></td>
<td><span data-ttu-id="4a7d9-121"><strong>1..10</strong> finnur öll gildi frá 1 til og með 10.</span><span class="sxs-lookup"><span data-stu-id="4a7d9-121"><strong>1..10</strong> finds all values from 1 through 10.</span></span> <span data-ttu-id="4a7d9-122">Á strengjasvæði finnur <strong>A..C</strong> aftur á móti öll gildi sem byrja á &quot;A&quot; og &quot;B&quot;, og gildi sem eru alveg jöfn &quot;C&quot;.</span><span class="sxs-lookup"><span data-stu-id="4a7d9-122">However, in a string field, <strong>A..C</strong> finds all values that start with &quot;A&quot; and &quot;B&quot;, and values that are exactly equal to &quot;C&quot;.</span></span> <span data-ttu-id="4a7d9-123">Til dæmis finnur þessi fyrirspurn ekki &quot;Ca&quot;.</span><span class="sxs-lookup"><span data-stu-id="4a7d9-123">For example, this query won't find &quot;Ca&quot;.</span></span> <span data-ttu-id="4a7d9-124">Til að finna öll gildi frá  &quot;A<em>&quot; til &quot;C</em>&quot;, færðu inn <strong>A..D</strong>.</span><span class="sxs-lookup"><span data-stu-id="4a7d9-124">To find all values from &quot;A<em>&quot; through &quot;C</em>&quot;, type <strong>A..D</strong>.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4a7d9-125"><em>gildi</em> (tvöfaldur punktur)</span><span class="sxs-lookup"><span data-stu-id="4a7d9-125">..<em>value</em> (double period)</span></span></td>
<td><span data-ttu-id="4a7d9-126">Minna en eða jafnt og gildið sem fært er inn.</span><span class="sxs-lookup"><span data-stu-id="4a7d9-126">Less than or equal to the value that is entered</span></span></td>
<td><span data-ttu-id="4a7d9-127">Færa inn tvo punkta og síðan gildið.</span><span class="sxs-lookup"><span data-stu-id="4a7d9-127">Type two periods and then the value.</span></span></td>
<td><span data-ttu-id="4a7d9-128"><strong>..1000</strong> finnur allar tölur sem eru minni en eða jafnar og 1000, t.d. &quot;100&quot;, &quot;999,95&quot; og &quot;1.000&quot;.</span><span class="sxs-lookup"><span data-stu-id="4a7d9-128"><strong>..1000</strong> finds any number that is less than or equal to 1000, such as &quot;100&quot;, &quot;999.95&quot;, and &quot;1,000&quot;.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4a7d9-129"><em>gildi</em>..</span><span class="sxs-lookup"><span data-stu-id="4a7d9-129"><em>value</em>..</span></span> <span data-ttu-id="4a7d9-130">(tveir punktar)</span><span class="sxs-lookup"><span data-stu-id="4a7d9-130">(double period)</span></span></td>
<td><span data-ttu-id="4a7d9-131">Meira en eða jafnt og gildið sem fært er inn.</span><span class="sxs-lookup"><span data-stu-id="4a7d9-131">Greater than or equal to the value that is entered</span></span></td>
<td><span data-ttu-id="4a7d9-132">Færa inn gildi og síðan tvo punkta.</span><span class="sxs-lookup"><span data-stu-id="4a7d9-132">Type the value and then two periods.</span></span></td>
<td><span data-ttu-id="4a7d9-133"><strong>1000 ..</strong></span><span class="sxs-lookup"><span data-stu-id="4a7d9-133"><strong>1000..</strong></span></span> <span data-ttu-id="4a7d9-134">1000.. finnur allar tölur sem eru meiri en eða jafnt og 1000, eins og &quot;1,000&quot;, &quot;1,000.01&quot;, og &quot;1,000,000&quot;.</span><span class="sxs-lookup"><span data-stu-id="4a7d9-134">finds any number that is greater than or equal to 1000, such as &quot;1,000&quot;, &quot;1,000.01&quot;, and &quot;1,000,000&quot;.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4a7d9-135">&gt;<em>gildi</em> (stærra en merki)</span><span class="sxs-lookup"><span data-stu-id="4a7d9-135">&gt;<em>value</em> (greater than sign)</span></span></td>
<td><span data-ttu-id="4a7d9-136">Stærra en gildið sem fært er inn.</span><span class="sxs-lookup"><span data-stu-id="4a7d9-136">Greater than the value that is entered</span></span></td>
<td><span data-ttu-id="4a7d9-137">Færðu inn stærra en-merki (<strong>&gt;</strong>) og síðan gildið.</span><span class="sxs-lookup"><span data-stu-id="4a7d9-137">Type a greater than sign (<strong>&gt;</strong>) and then the value.</span></span></td>
<td><span data-ttu-id="4a7d9-138"><strong>&gt;1000</strong> finnur allar tölur sem eru meiri en 1000, eins og &quot;1000.01&quot;, &quot;20,000&quot;, og &quot;1,000,000&quot;.</span><span class="sxs-lookup"><span data-stu-id="4a7d9-138"><strong>&gt;1000</strong> finds any number that is greater than 1000, such as &quot;1000.01&quot;, &quot;20,000&quot;, and &quot;1,000,000&quot;.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4a7d9-139">&lt;<em>gildi</em> (minna en merki)</span><span class="sxs-lookup"><span data-stu-id="4a7d9-139">&lt;<em>value</em> (less than sign)</span></span></td>
<td><span data-ttu-id="4a7d9-140">Minna en gildið sem fært er inn.</span><span class="sxs-lookup"><span data-stu-id="4a7d9-140">Less than the value that is entered</span></span></td>
<td><span data-ttu-id="4a7d9-141">Færðu inn minna en-merki (<strong>&lt;</strong>) og síðan gildið.</span><span class="sxs-lookup"><span data-stu-id="4a7d9-141">Type a less than sign (<strong>&lt;</strong>) and then the value.</span></span></td>
<td><span data-ttu-id="4a7d9-142"><strong>&lt;1000</strong> finnur allar tölur sem eru minni en 1000, eins og &quot;999.99&quot;, &quot;1&quot;, og  &quot;-200&quot;.</span><span class="sxs-lookup"><span data-stu-id="4a7d9-142"><strong>&lt;1000</strong> finds any number that is less than 1000, such as &quot;999.99&quot;, &quot;1&quot;, and &quot;-200&quot;.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4a7d9-143"><em>gildi</em>\* (stjarna)</span><span class="sxs-lookup"><span data-stu-id="4a7d9-143"><em>value</em>\* (asterisk)</span></span></td>
<td><span data-ttu-id="4a7d9-144">Byrjar frá gildið sem fært er inn.</span><span class="sxs-lookup"><span data-stu-id="4a7d9-144">Starting from the value that is entered</span></span></td>
<td><span data-ttu-id="4a7d9-145">Færa inn upphafsgildið og síðan stjörnuna (<strong>\*</strong>)</span><span class="sxs-lookup"><span data-stu-id="4a7d9-145">Type the starting value and then an asterisk (<strong>\*</strong>).</span></span></td>
<td><span data-ttu-id="4a7d9-146"><strong>S\*</strong> finnur alla strengi sem byrja á &quot;S&quot;, eins og &quot;Stokkhólmur&quot;, &quot;Sydney&quot; og &quot;San Francisco&quot;.</span><span class="sxs-lookup"><span data-stu-id="4a7d9-146"><strong>S\*</strong> finds any string that starts with &quot;S&quot;, such as &quot;Stockholm&quot;, &quot;Sydney&quot;, and &quot;San Francisco&quot;.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4a7d9-147">\*<em>gildi</em> (stjarna)</span><span class="sxs-lookup"><span data-stu-id="4a7d9-147">\*<em>value</em> (asterisk)</span></span></td>
<td><span data-ttu-id="4a7d9-148">Endar á gildið sem fært er inn.</span><span class="sxs-lookup"><span data-stu-id="4a7d9-148">Ending with the value that is entered</span></span></td>
<td><span data-ttu-id="4a7d9-149">Færa inn stjörnu og síðan endagildið.</span><span class="sxs-lookup"><span data-stu-id="4a7d9-149">Type an asterisk and then the ending value.</span></span></td>
<td><span data-ttu-id="4a7d9-150"><strong>\*austur</strong> finnur alla strengi sem enda á &quot;austur&quot;, eins og &quot;Norðaustur&quot; og &quot;Suðaustur&quot;.</span><span class="sxs-lookup"><span data-stu-id="4a7d9-150"><strong>\*east</strong> finds any string that ends with &quot;east&quot;, such as &quot;Northeast&quot; and &quot;Southeast&quot;.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4a7d9-151">*<em>gildi</em>* (stjarna)</span><span class="sxs-lookup"><span data-stu-id="4a7d9-151">*<em>value</em>* (asterisk)</span></span></td>
<td><span data-ttu-id="4a7d9-152">Inniheldur gildið sem fært er inn.</span><span class="sxs-lookup"><span data-stu-id="4a7d9-152">Containing the value that is entered</span></span></td>
<td><span data-ttu-id="4a7d9-153">Færa inn stjörnu, gildi og síðan aðra stjörnu.</span><span class="sxs-lookup"><span data-stu-id="4a7d9-153">Type an asterisk, then a value, and then another asterisk.</span></span></td>
<td><span data-ttu-id="4a7d9-154"><strong>*rð*</strong> finnur alla strengi sem innihalda &quot;rð&quot;, eins og &quot;Norðaustur&quot; og &quot;Suðaustur&quot;.</span><span class="sxs-lookup"><span data-stu-id="4a7d9-154"><strong>*th*</strong> finds any string that contains &quot;th&quot;, such as &quot;Northeast&quot; and &quot;Southeast&quot;.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4a7d9-155">?</span><span class="sxs-lookup"><span data-stu-id="4a7d9-155">?</span></span> <span data-ttu-id="4a7d9-156">(spurningamerki)</span><span class="sxs-lookup"><span data-stu-id="4a7d9-156">(question mark)</span></span></td>
<td><span data-ttu-id="4a7d9-157">Innihalda einn eða fleiri óþekkta stafi</span><span class="sxs-lookup"><span data-stu-id="4a7d9-157">Having one or more unknown characters</span></span></td>
<td><span data-ttu-id="4a7d9-158">Færðu inn spurningamerki við stöðu óþekkts staftákns í gildinu.</span><span class="sxs-lookup"><span data-stu-id="4a7d9-158">Type a question mark at the position of the unknown character in the value.</span></span></td>
<td><span data-ttu-id="4a7d9-159"><strong>Sm?th</strong> finnur &quot;Smith&quot; og &quot;Smyth&quot;.</span><span class="sxs-lookup"><span data-stu-id="4a7d9-159"><strong>Sm?th</strong> finds &quot;Smith&quot; and &quot;Smyth&quot;.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4a7d9-160"><em>gildi</em>,<em>gildi</em> (komma)</span><span class="sxs-lookup"><span data-stu-id="4a7d9-160"><em>value</em>,<em>value</em> (comma)</span></span></td>
<td><span data-ttu-id="4a7d9-161">Samsvarar gildunum sem eru aðskilin með kommum.</span><span class="sxs-lookup"><span data-stu-id="4a7d9-161">Matching the values that are separated by commas</span></span></td>
<td><span data-ttu-id="4a7d9-162">Færa inn öll þín skilyrði, og aðskiljið þau með kommu.</span><span class="sxs-lookup"><span data-stu-id="4a7d9-162">Type all your criteria, and separate them by using commas.</span></span></td>
<td><span data-ttu-id="4a7d9-163"><strong>A, D, F, G</strong> finnur nákvæmlega &quot;A&quot;, &quot;D&quot;, &quot;F&quot;, og &quot;G&quot;.</span><span class="sxs-lookup"><span data-stu-id="4a7d9-163"><strong>A, D, F, G</strong> finds exactly &quot;A&quot;, &quot;D&quot;, &quot;F&quot;, and &quot;G&quot;.</span></span> <span data-ttu-id="4a7d9-164"><strong>10, 20, 30, 100</strong> finnur nákvæmlega &quot;10, 20, 30, 100&quot;.</span><span class="sxs-lookup"><span data-stu-id="4a7d9-164"><strong>10, 20, 30, 100</strong> finds exactly &quot;10, 20, 30, 100&quot;.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4a7d9-165">(<span class="code">Sql-strengur</span>) (Sql-strengur milli sviga)</span><span class="sxs-lookup"><span data-stu-id="4a7d9-165">(<span class="code">SQL statement</span>) (SQL statement between parentheses)</span></span></td>
<td><span data-ttu-id="4a7d9-166">Samsvarar tilgreindri fyrirspurn</span><span class="sxs-lookup"><span data-stu-id="4a7d9-166">Matching a defined query</span></span></td>
<td><span data-ttu-id="4a7d9-167">Færa inn fyrirspurn sem SQL-skipun innan sviga.</span><span class="sxs-lookup"><span data-stu-id="4a7d9-167">Type a query as an SQL statement between parentheses.</span></span></td>
<td><span data-ttu-id="4a7d9-168"><strong><span class="code">(gagnaveita.reitarheiti != &quot;A&quot;)</span></strong></span><span class="sxs-lookup"><span data-stu-id="4a7d9-168"><strong><span class="code">(data source.Fieldname != &quot;A&quot;)</span></strong></span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4a7d9-169">Þ</span><span class="sxs-lookup"><span data-stu-id="4a7d9-169">T</span></span></td>
<td><span data-ttu-id="4a7d9-170">Dagurinn í dag</span><span class="sxs-lookup"><span data-stu-id="4a7d9-170">Today's date</span></span></td>
<td><span data-ttu-id="4a7d9-171">gerð <strong>T</strong>.</span><span class="sxs-lookup"><span data-stu-id="4a7d9-171">Type <strong>T</strong>.</span></span></td>
<td><span data-ttu-id="4a7d9-172"><strong>T</strong> samsvarar dagurinn í dag.</span><span class="sxs-lookup"><span data-stu-id="4a7d9-172"><strong>T</strong> matches today's date.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4a7d9-173">(methodName(parameters)) (<strong>SysQueryRangeUtil</strong> aðferð á milli sviga)</span><span class="sxs-lookup"><span data-stu-id="4a7d9-173">(methodName(parameters)) (<strong>SysQueryRangeUtil</strong> method between parentheses)</span></span></td>
<td><span data-ttu-id="4a7d9-174">Jöfnun gilda eða bil gilda sem eru tilgreind í færibreytum <strong>SysQueryRangeUtil</strong> aðferð</span><span class="sxs-lookup"><span data-stu-id="4a7d9-174">Matching the value or range of values that are specified by the parameters of the <strong>SysQueryRangeUtil</strong> method</span></span></td>
<td><span data-ttu-id="4a7d9-175">Færðu inn <strong>SysQueryRangeUtil</strong> aðferð sem er með færibreytum sem tilgreina gildi eða svið gilda.</span><span class="sxs-lookup"><span data-stu-id="4a7d9-175">Type a <strong>SysQueryRangeUtil</strong> method that has parameters that specify the value or range of values.</span></span></td>
<td>
<ol>
<li><span data-ttu-id="4a7d9-176">Smellt er á <strong>Viðskiptakröfur</strong> &gt; <strong>Reikningar</strong> &gt; <strong>Opið reikning viðskiptavinar</strong>.</span><span class="sxs-lookup"><span data-stu-id="4a7d9-176">Click <strong>Accounts receivable</strong> &gt; <strong>Invoices</strong> &gt; <strong>Open customer invoices</strong>.</span></span></li>
<li><span data-ttu-id="4a7d9-177">Styðjið á Ctrl + Shift + F3 til að opna í <strong>Fyrirspurn</strong> síðu.</span><span class="sxs-lookup"><span data-stu-id="4a7d9-177">Press Ctrl+Shift+F3 to open the <strong>Inquiry</strong> page.</span></span></li>
<li><span data-ttu-id="4a7d9-178">Á flipanum <strong>svið</strong>, er smellt á <strong>Bæta við</strong>.</span><span class="sxs-lookup"><span data-stu-id="4a7d9-178">On the <strong>Range</strong> tab, click <strong>Add</strong>.</span></span></li>
<li><span data-ttu-id="4a7d9-179">Í <strong>töflu</strong> reit, velja<strong>opnar færsla viðskiptavinar</strong>.</span><span class="sxs-lookup"><span data-stu-id="4a7d9-179">In the <strong>Table</strong> field, select <strong>Open customer transactions</strong>.</span></span></li>
<li><span data-ttu-id="4a7d9-180">Á svæðinu <strong>reitur</strong>velja<strong>gjalddagi</strong></span><span class="sxs-lookup"><span data-stu-id="4a7d9-180">In the <strong>Field</strong> field, select <strong>Due date</strong>.</span></span></li>
<li><span data-ttu-id="4a7d9-181">Í <strong>skilyrði</strong> reitnum, færa inn <strong>(yearRange(-2,0))</strong>.</span><span class="sxs-lookup"><span data-stu-id="4a7d9-181">In the <strong>Criteria</strong> field, enter <strong>(yearRange(-2,0))</strong>.</span></span></li>
<li><span data-ttu-id="4a7d9-182">Smelltu á <strong>Í lagi</strong>.</span><span class="sxs-lookup"><span data-stu-id="4a7d9-182">Click <strong>OK</strong>.</span></span> <span data-ttu-id="4a7d9-183">listasíða er uppfærð til að birta lista yfir reikninga sem stemma við skilyrði sem þú færðir inn.</span><span class="sxs-lookup"><span data-stu-id="4a7d9-183">The list page is updated and lists the invoices that match the criterion that you entered.</span></span> <span data-ttu-id="4a7d9-184">Í þessu dæmi eru reikningar sem voru á gjalddaga síðustu tvö ár taldir upp.</span><span class="sxs-lookup"><span data-stu-id="4a7d9-184">For this example, invoices that were due in the previous two years are listed.</span></span></li>
</ol>
<span data-ttu-id="4a7d9-185">Sjá töfluna í næsta hluta fyrir frekari upplýsingar um <strong>SysQueryRangeUtil</strong> dagsetningaraðferðir og nokkur dæmi.</span><span class="sxs-lookup"><span data-stu-id="4a7d9-185">See the table in the next section for additional details about <strong>SysQueryRangeUtil</strong> date methods, and several examples.</span></span></td>
</tr>
</tbody>
</table>

## <a name="advanced-date-queries-that-use-sysqueryrangeutil-methods"></a><span data-ttu-id="4a7d9-186">ítarlega dagsetningarfyrirspurnir sem nota SysQueryRangeUtil aðferðir</span><span class="sxs-lookup"><span data-stu-id="4a7d9-186">Advanced date queries that use SysQueryRangeUtil methods</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="4a7d9-187">Aðferð</span><span class="sxs-lookup"><span data-stu-id="4a7d9-187">Method</span></span></th>
<th><span data-ttu-id="4a7d9-188">Lýsing</span><span class="sxs-lookup"><span data-stu-id="4a7d9-188">Description</span></span></th>
<th><span data-ttu-id="4a7d9-189">Dæmi</span><span class="sxs-lookup"><span data-stu-id="4a7d9-189">Example</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4a7d9-190">Dagur (_relativeDays=0)</span><span class="sxs-lookup"><span data-stu-id="4a7d9-190">Day (_relativeDays=0)</span></span></td>
<td><span data-ttu-id="4a7d9-191">Finna dagsetningu miðað við dagsetningu setu.</span><span class="sxs-lookup"><span data-stu-id="4a7d9-191">Find a date relative to the session date.</span></span> <span data-ttu-id="4a7d9-192">Jákvæð gildi tilgreina framtíðardagsetningar, og neikvæð gildi tilgreina liðnar dagsetningar.</span><span class="sxs-lookup"><span data-stu-id="4a7d9-192">Positive values indicate future dates, and negative values indicate past dates.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="4a7d9-193"><strong>Á morgun</strong> – færðu inn<strong>(dagur(1))</strong>.</span><span class="sxs-lookup"><span data-stu-id="4a7d9-193"><strong>Tomorrow</strong> – Enter <strong>(Day(1))</strong>.</span></span></li>
<li><span data-ttu-id="4a7d9-194"><strong>Í dag</strong> – Færðu inn<strong>(dagur(0))</strong>.</span><span class="sxs-lookup"><span data-stu-id="4a7d9-194"><strong>Today</strong> – Enter <strong>(Day(0))</strong>.</span></span></li>
<li><span data-ttu-id="4a7d9-195"><strong>Í gær</strong> – færðu inn<strong>(dagur(-1))</strong>.</span><span class="sxs-lookup"><span data-stu-id="4a7d9-195"><strong>Yesterday</strong> – Enter <strong>(Day(-1))</strong>.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="4a7d9-196">DayRange (_relativeDaysFrom=0, _relativeDaysTo=0)</span><span class="sxs-lookup"><span data-stu-id="4a7d9-196">DayRange (_relativeDaysFrom=0, _relativeDaysTo=0)</span></span></td>
<td><span data-ttu-id="4a7d9-197">Finna dagsetningarsvið miðað við dagsetningu setu.</span><span class="sxs-lookup"><span data-stu-id="4a7d9-197">Find a range of dates relative to the session date.</span></span> <span data-ttu-id="4a7d9-198">Jákvæð gildi tilgreina framtíðardagsetningar, og neikvæð gildi tilgreina liðnar dagsetningar.</span><span class="sxs-lookup"><span data-stu-id="4a7d9-198">Positive values indicate future dates, and negative values indicate past dates.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="4a7d9-199"><strong>Síðustu 30 daga </strong> - Sláðu inn <strong>" (DayRange (-30,0))</strong></span><span class="sxs-lookup"><span data-stu-id="4a7d9-199"><strong>Last 30 days</strong> – Enter <strong>(DayRange(-30,0))</strong>.</span></span></li>
<li><span data-ttu-id="4a7d9-200"><strong>Fyrri 30 dagar og næstu 30 dagar </strong>– færið inn <strong>“(DayRange(-30,30))”</strong></span><span class="sxs-lookup"><span data-stu-id="4a7d9-200"><strong>Previous 30 days and next 30 days</strong> – Enter <strong>(DayRange(-30,30))</strong>.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="4a7d9-201">GreaterThanDate (_relativeDays=0) GreaterThanUtcDate (_relativeDays=0)</span><span class="sxs-lookup"><span data-stu-id="4a7d9-201">GreaterThanDate (_relativeDays=0) GreaterThanUtcDate (_relativeDays=0)</span></span></td>
<td><span data-ttu-id="4a7d9-202">Leita að öllum dagsetningum eftir tilgreinda afstæða dagsetningu.</span><span class="sxs-lookup"><span data-stu-id="4a7d9-202">Find all dates after the specified relative date.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="4a7d9-203"><strong>Meira en 30 dagar frá því núna</strong> – færið Inn <strong>(GreaterThanDate(30))</strong>.</span><span class="sxs-lookup"><span data-stu-id="4a7d9-203"><strong>More than 30 days from now</strong> – Enter <strong>(GreaterThanDate(30))</strong>.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="4a7d9-204">GreaterThanUtcNow ()</span><span class="sxs-lookup"><span data-stu-id="4a7d9-204">GreaterThanUtcNow ()</span></span></td>
<td><span data-ttu-id="4a7d9-205">Finna allar færslur dagsetningar/tíma eftir núverandi tíma.</span><span class="sxs-lookup"><span data-stu-id="4a7d9-205">Find all date/time entries after the current time.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="4a7d9-206"><strong>Allar framtíðar dagsetningar/tími</strong> – færið Inn <strong>(GreaterThanUtcNow())</strong>.</span><span class="sxs-lookup"><span data-stu-id="4a7d9-206"><strong>All future date/times</strong> – Enter <strong>(GreaterThanUtcNow())</strong>.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="4a7d9-207">LessThanDate (_relativeDays=0) LessThanUtcDate (_relativeDays=0)</span><span class="sxs-lookup"><span data-stu-id="4a7d9-207">LessThanDate (_relativeDays=0) LessThanUtcDate (_relativeDays=0)</span></span></td>
<td><span data-ttu-id="4a7d9-208">Leita að öllum dagsetningum fyrir tilgreinda afstæða dagsetningu.</span><span class="sxs-lookup"><span data-stu-id="4a7d9-208">Find all dates before the specified relative date.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="4a7d9-209"><strong>Minna en sjö dagar frá núna</strong> – færið Inn <strong>(LessThanDate(7))</strong>.</span><span class="sxs-lookup"><span data-stu-id="4a7d9-209"><strong>Less than seven days from now</strong> – Enter <strong>(LessThanDate(7))</strong>.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="4a7d9-210">LessThanUtcNow ()</span><span class="sxs-lookup"><span data-stu-id="4a7d9-210">LessThanUtcNow ()</span></span></td>
<td><span data-ttu-id="4a7d9-211">Finna allar færslur dagsetningar/tíma fyrir núverandi tíma.</span><span class="sxs-lookup"><span data-stu-id="4a7d9-211">Find all date/time entries before the current time.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="4a7d9-212"><strong>Allar liðnar dagsetningu/tíma</strong> – færið Inn <strong>(LessThanUtcNow())</strong>.</span><span class="sxs-lookup"><span data-stu-id="4a7d9-212"><strong>All past date/times</strong> – Enter <strong>(LessThanUtcNow())</strong>.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="4a7d9-213">MonthRange (_relativeFrom=0, _relativeTo=0)</span><span class="sxs-lookup"><span data-stu-id="4a7d9-213">MonthRange (_relativeFrom=0, _relativeTo=0)</span></span></td>
<td><span data-ttu-id="4a7d9-214">Finna svið dagsetninga samkvæmt mánaða samanborið við núverandi mánuð</span><span class="sxs-lookup"><span data-stu-id="4a7d9-214">Find a range of dates, based on months relative to the current month.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="4a7d9-215"><strong>Fyrri tveir mánuðir</strong> – færið Inn <strong>(MonthRange(-2,0))</strong>.</span><span class="sxs-lookup"><span data-stu-id="4a7d9-215"><strong>Previous two months</strong> – Enter <strong>(MonthRange(-2,0))</strong>.</span></span></li>
<li><span data-ttu-id="4a7d9-216"><strong>Næstu þrír mánuðir</strong> – færið Inn <strong>(MonthRange(0,3))</strong>.</span><span class="sxs-lookup"><span data-stu-id="4a7d9-216"><strong>Next three months</strong> – Enter <strong>(MonthRange(0,3))</strong>.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="4a7d9-217">YearRange (_relativeFrom=0, _relativeTo=0)</span><span class="sxs-lookup"><span data-stu-id="4a7d9-217">YearRange (_relativeFrom=0, _relativeTo=0)</span></span></td>
<td><span data-ttu-id="4a7d9-218">Finna svið dagsetninga samkvæmt árum samanborið við í núverandi ár.</span><span class="sxs-lookup"><span data-stu-id="4a7d9-218">Find a range of dates, based on years relative to the current year.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="4a7d9-219"><strong>Næsta árs</strong> – færið Inn <strong>(YearRange (0, 1))</strong>.</span><span class="sxs-lookup"><span data-stu-id="4a7d9-219"><strong>Next year</strong> – Enter <strong>(YearRange(0, 1))</strong>.</span></span></li>
<li><span data-ttu-id="4a7d9-220"><strong>Fyrra ár</strong> – Færið Inn <strong>(YearRange (-1,0))</strong>.</span><span class="sxs-lookup"><span data-stu-id="4a7d9-220"><strong>Previous year</strong> – Enter <strong>(YearRange(-1,0))</strong>.</span></span></li>
</ul>
</td>
</tr>
</tbody>
</table>
