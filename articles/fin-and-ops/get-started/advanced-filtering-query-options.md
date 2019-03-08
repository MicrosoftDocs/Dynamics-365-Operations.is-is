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
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/29/2019
ms.locfileid: "355956"
---
# <a name="advanced-filtering-and-query-syntax"></a>Ítarleg sía og málskipan fyrirspurna

[!include [banner](../includes/banner.md)]

Þessi grein lýsir síunar- og fyrirspurnarmöguleikum sem eru tiltækar þegar þú notar svargluggann fyrir sía/raða ítarlega eða **samsvörun** virknitáknið á síusvæðinu eða síur fyrir dálkhaus hnitanets.

## <a name="advanced-query-syntax"></a>Ítarleg fyrirspurnarmálskipan

<table>
<thead>
<tr>
<th>Málskipun</th>
<th>Lýsing á tákni</th>
<th>lýsing</th>
<th>Dæmi</th>
</tr>
</thead>
<tbody>
<tr>
<td><em>gildi</em></td>
<td>jafnt og gildið sem fært var inn.</td>
<td>Sláið inn gildi til að finna.</td>
<td><strong>Smith</strong> finnur &quot;Smith&quot;.</td>
</tr>
<tr>
<td>!<em>-gildi</em> (upphrópunarmerki)</td>
<td>Ekki jafnt og gildið sem fært var inn.</td>
<td>Færðu inn upphrópunarmerki og síðan gildið til að undanskilja.</td>
<td><strong>!Smith</strong> finnur öll gildi nema &quot;Smith&quot;.</td>
</tr>
<tr>
<td><em>frá-gildi</em>..<em>til- gildi</em> (tvöfaldur punktur)</td>
<td>Á milli tveggja gilda sem eru inn aðskilin með tveimur punktum.</td>
<td>Færa inn Frá gildið, færa svo inn tvo punkta og síðan Til gildið.</td>
<td><strong>1..10</strong> finnur öll gildi frá 1 til og með 10. Á strengjasvæði finnur <strong>A..C</strong> aftur á móti öll gildi sem byrja á &quot;A&quot; og &quot;B&quot;, og gildi sem eru alveg jöfn &quot;C&quot;. Til dæmis finnur þessi fyrirspurn ekki &quot;Ca&quot;. Til að finna öll gildi frá  &quot;A<em>&quot; til &quot;C</em>&quot;, færðu inn <strong>A..D</strong>.</td>
</tr>
<tr>
<td><em>gildi</em> (tvöfaldur punktur)</td>
<td>Minna en eða jafnt og gildið sem fært er inn.</td>
<td>Færa inn tvo punkta og síðan gildið.</td>
<td><strong>..1000</strong> finnur allar tölur sem eru minni en eða jafnar og 1000, t.d. &quot;100&quot;, &quot;999,95&quot; og &quot;1.000&quot;.</td>
</tr>
<tr>
<td><em>gildi</em>.. (tveir punktar)</td>
<td>Meira en eða jafnt og gildið sem fært er inn.</td>
<td>Færa inn gildi og síðan tvo punkta.</td>
<td><strong>1000 ..</strong> 1000.. finnur allar tölur sem eru meiri en eða jafnt og 1000, eins og &quot;1,000&quot;, &quot;1,000.01&quot;, og &quot;1,000,000&quot;.</td>
</tr>
<tr>
<td>&gt;<em>gildi</em> (stærra en merki)</td>
<td>Stærra en gildið sem fært er inn.</td>
<td>Færðu inn stærra en-merki (<strong>&gt;</strong>) og síðan gildið.</td>
<td><strong>&gt;1000</strong> finnur allar tölur sem eru meiri en 1000, eins og &quot;1000.01&quot;, &quot;20,000&quot;, og &quot;1,000,000&quot;.</td>
</tr>
<tr>
<td>&lt;<em>gildi</em> (minna en merki)</td>
<td>Minna en gildið sem fært er inn.</td>
<td>Færðu inn minna en-merki (<strong>&lt;</strong>) og síðan gildið.</td>
<td><strong>&lt;1000</strong> finnur allar tölur sem eru minni en 1000, eins og &quot;999.99&quot;, &quot;1&quot;, og  &quot;-200&quot;.</td>
</tr>
<tr>
<td><em>gildi</em>* (stjarna)</td>
<td>Byrjar frá gildið sem fært er inn.</td>
<td>Færa inn upphafsgildið og síðan stjörnuna (<strong>*</strong>)</td>
<td><strong>S*</strong> finnur alla strengi sem byrja á &quot;S&quot;, eins og &quot;Stokkhólmur&quot;, &quot;Sydney&quot; og &quot;San Francisco&quot;.</td>
</tr>
<tr>
<td>*<em>gildi</em> (stjarna)</td>
<td>Endar á gildið sem fært er inn.</td>
<td>Færa inn stjörnu og síðan endagildið.</td>
<td><strong>*austur</strong> finnur alla strengi sem enda á &quot;austur&quot;, eins og &quot;Norðaustur&quot; og &quot;Suðaustur&quot;.</td>
</tr>
<tr>
<td>*<em>gildi</em>* (stjarna)</td>
<td>Inniheldur gildið sem fært er inn.</td>
<td>Færa inn stjörnu, gildi og síðan aðra stjörnu.</td>
<td><strong>*rð*</strong> finnur alla strengi sem innihalda &quot;rð&quot;, eins og &quot;Norðaustur&quot; og &quot;Suðaustur&quot;.</td>
</tr>
<tr>
<td>? (spurningamerki)</td>
<td>Innihalda einn eða fleiri óþekkta stafi</td>
<td>Færðu inn spurningamerki við stöðu óþekkts staftákns í gildinu.</td>
<td><strong>Sm?th</strong> finnur &quot;Smith&quot; og &quot;Smyth&quot;.</td>
</tr>
<tr>
<td><em>gildi</em>,<em>gildi</em> (komma)</td>
<td>Samsvarar gildunum sem eru aðskilin með kommum.</td>
<td>Færa inn öll þín skilyrði, og aðskiljið þau með kommu.</td>
<td><strong>A, D, F, G</strong> finnur nákvæmlega &quot;A&quot;, &quot;D&quot;, &quot;F&quot;, og &quot;G&quot;. <strong>10, 20, 30, 100</strong> finnur nákvæmlega &quot;10, 20, 30, 100&quot;.</td>
</tr>
<tr>
<td>(<span class="code">Sql-strengur</span>) (Sql-strengur milli sviga)</td>
<td>Samsvarar tilgreindri fyrirspurn</td>
<td>Færa inn fyrirspurn sem SQL-skipun innan sviga.</td>
<td><strong><span class="code">(gagnaveita.reitarheiti != &quot;A&quot;)</span></strong></td>
</tr>
<tr>
<td>Þ</td>
<td>Dagurinn í dag</td>
<td>gerð <strong>T</strong>.</td>
<td><strong>T</strong> samsvarar dagurinn í dag.</td>
</tr>
<tr>
<td>(methodName(parameters)) (<strong>SysQueryRangeUtil</strong> aðferð á milli sviga)</td>
<td>Jöfnun gilda eða bil gilda sem eru tilgreind í færibreytum <strong>SysQueryRangeUtil</strong> aðferð</td>
<td>Færðu inn <strong>SysQueryRangeUtil</strong> aðferð sem er með færibreytum sem tilgreina gildi eða svið gilda.</td>
<td>
<ol>
<li>Smellt er á <strong>Viðskiptakröfur</strong> &gt; <strong>Reikningar</strong> &gt; <strong>Opið reikning viðskiptavinar</strong>.</li>
<li>Styðjið á Ctrl + Shift + F3 til að opna í <strong>Fyrirspurn</strong> síðu.</li>
<li>Á flipanum <strong>svið</strong>, er smellt á <strong>Bæta við</strong>.</li>
<li>Í <strong>töflu</strong> reit, velja<strong>opnar færsla viðskiptavinar</strong>.</li>
<li>Á svæðinu <strong>reitur</strong>velja<strong>gjalddagi</strong></li>
<li>Í <strong>skilyrði</strong> reitnum, færa inn <strong>(yearRange(-2,0))</strong>.</li>
<li>Smelltu á <strong>Í lagi</strong>. listasíða er uppfærð til að birta lista yfir reikninga sem stemma við skilyrði sem þú færðir inn. Í þessu dæmi eru reikningar sem voru á gjalddaga síðustu tvö ár taldir upp.</li>
</ol>
Sjá töfluna í næsta hluta fyrir frekari upplýsingar um <strong>SysQueryRangeUtil</strong> dagsetningaraðferðir og nokkur dæmi.</td>
</tr>
</tbody>
</table>

## <a name="advanced-date-queries-that-use-sysqueryrangeutil-methods"></a>ítarlega dagsetningarfyrirspurnir sem nota SysQueryRangeUtil aðferðir

<table>
<thead>
<tr>
<th>Aðferð</th>
<th>Lýsing</th>
<th>Dæmi</th>
</tr>
</thead>
<tbody>
<tr>
<td>Dagur (_relativeDays=0)</td>
<td>Finna dagsetningu miðað við dagsetningu setu. Jákvæð gildi tilgreina framtíðardagsetningar, og neikvæð gildi tilgreina liðnar dagsetningar.</td>
<td>
<ul>
<li><strong>Á morgun</strong> – færðu inn<strong>(dagur(1))</strong>.</li>
<li><strong>Í dag</strong> – Færðu inn<strong>(dagur(0))</strong>.</li>
<li><strong>Í gær</strong> – færðu inn<strong>(dagur(-1))</strong>.</li>
</ul>
</td>
</tr>
<tr>
<td>DayRange (_relativeDaysFrom=0, _relativeDaysTo=0)</td>
<td>Finna dagsetningarsvið miðað við dagsetningu setu. Jákvæð gildi tilgreina framtíðardagsetningar, og neikvæð gildi tilgreina liðnar dagsetningar.</td>
<td>
<ul>
<li><strong>Síðustu 30 daga </strong> - Sláðu inn <strong>" (DayRange (-30,0))</strong></li>
<li><strong>Fyrri 30 dagar og næstu 30 dagar </strong>– færið inn <strong>“(DayRange(-30,30))”</strong></li>
</ul>
</td>
</tr>
<tr>
<td>GreaterThanDate (_relativeDays=0) GreaterThanUtcDate (_relativeDays=0)</td>
<td>Leita að öllum dagsetningum eftir tilgreinda afstæða dagsetningu.</td>
<td>
<ul>
<li><strong>Meira en 30 dagar frá því núna</strong> – færið Inn <strong>(GreaterThanDate(30))</strong>.</li>
</ul>
</td>
</tr>
<tr>
<td>GreaterThanUtcNow ()</td>
<td>Finna allar færslur dagsetningar/tíma eftir núverandi tíma.</td>
<td>
<ul>
<li><strong>Allar framtíðar dagsetningar/tími</strong> – færið Inn <strong>(GreaterThanUtcNow())</strong>.</li>
</ul>
</td>
</tr>
<tr>
<td>LessThanDate (_relativeDays=0) LessThanUtcDate (_relativeDays=0)</td>
<td>Leita að öllum dagsetningum fyrir tilgreinda afstæða dagsetningu.</td>
<td>
<ul>
<li><strong>Minna en sjö dagar frá núna</strong> – færið Inn <strong>(LessThanDate(7))</strong>.</li>
</ul>
</td>
</tr>
<tr>
<td>LessThanUtcNow ()</td>
<td>Finna allar færslur dagsetningar/tíma fyrir núverandi tíma.</td>
<td>
<ul>
<li><strong>Allar liðnar dagsetningu/tíma</strong> – færið Inn <strong>(LessThanUtcNow())</strong>.</li>
</ul>
</td>
</tr>
<tr>
<td>MonthRange (_relativeFrom=0, _relativeTo=0)</td>
<td>Finna svið dagsetninga samkvæmt mánaða samanborið við núverandi mánuð</td>
<td>
<ul>
<li><strong>Fyrri tveir mánuðir</strong> – færið Inn <strong>(MonthRange(-2,0))</strong>.</li>
<li><strong>Næstu þrír mánuðir</strong> – færið Inn <strong>(MonthRange(0,3))</strong>.</li>
</ul>
</td>
</tr>
<tr>
<td>YearRange (_relativeFrom=0, _relativeTo=0)</td>
<td>Finna svið dagsetninga samkvæmt árum samanborið við í núverandi ár.</td>
<td>
<ul>
<li><strong>Næsta árs</strong> – færið Inn <strong>(YearRange (0, 1))</strong>.</li>
<li><strong>Fyrra ár</strong> – Færið Inn <strong>(YearRange (-1,0))</strong>.</li>
</ul>
</td>
</tr>
</tbody>
</table>
