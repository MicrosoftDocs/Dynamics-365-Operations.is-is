---
title: "Segðarskorður og töfluskorður í afbrigðalíkönum afurðar"
description: "Þetta efnisatriði lýsir notkun skorður segð og töfluskorðum. Skorður stjórna eigindargildin sem hægt er að velja þegar afurðir fyrir sölupöntun, sölutilboði, innkaupapöntun eða framleiðslupöntun. Hægt er að nota skorður segð eða töfluskorðum, eftir því hvernig óskað er að byggja á skorðum."
author: cvocph
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PCGlobalTableConstraintEdit, PCProductConfigurationModelDetails, PCTableConstraintAttachAttributeTree, PCTableConstraintDefinition
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Core, Operations
ms.custom: 53111
ms.assetid: 5c12b1f2-eb89-4648-a755-de412f2eadd6
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: e4719ace2247eb95ed711b0c82e7d9bc8ec5c60c
ms.contentlocale: is-is
ms.lasthandoff: 11/03/2017

---

# <a name="expression-constraints-and-table-constraints-in-product-configuration-models"></a>Segðarskorður og töfluskorður í afbrigðalíkönum afurðar

[!include[banner](../includes/banner.md)]


Þetta efnisatriði lýsir notkun skorður segð og töfluskorðum. Skorður stjórna eigindargildin sem hægt er að velja þegar afurðir fyrir sölupöntun, sölutilboði, innkaupapöntun eða framleiðslupöntun. Hægt er að nota skorður segð eða töfluskorðum, eftir því hvernig óskað er að byggja á skorðum. 

Skorður eru notaðar til að stjórna eigindargildin sem hægt er að velja þegar afurðir fyrir sölupöntun, sölutilboði, innkaupapöntun eða framleiðslupöntun. Hægt er að nota skorður segð eða töfluskorðum, eftir því hvernig óskað er að byggja á skorðum.

## <a name="what-are-expression-constraints"></a>Hvað eru segðaskorður?
Segð skorður eru auðkennd með segð sem notar virkjar arithmetic og Boole og aðgerðir. Segðarþvingun er skrifað fyrir ákveðna íhluti í afbrigðalíkan afurðar. Það er ekki hægt að endurnýta með eða deilt með öðrum íhlut. Segðarskorðurnar fyrir íhlut geta hins vegar vísað í eigindir undiríhluta íhlutarins.

## <a name="what-are-table-constraints"></a>Hvað eru töfluskorðum?
Töfluskorður skrá samsetningargildi sem eru leyfðar fyrir eiginleika þegar þú stillir afurð. Skilgreiningar töfluskorðu er hægt að nota almennt. Þegar töfluskorða fyrir íhlut í afbrigðalíkani afurðar er stofnað skaltu velja skilgreiningu töfluskorðu. Til að stofna samsetningar sem eru leyfðar bætirðu við eigindum ákveðinna gerða íhluta. Hver gerð eigindar hefur ákveðið gildi.

### <a name="example-of-a-table-constraint"></a>Dæmi um töfluskorðu

Þetta dæmi sýnir hvernig hægt er að takmarka skilgreiningu hátalara við tiltekinn frágang húss og framhliðir. Fyrsta taflan sýnir frágang húss og framhliðir sem eru almennt aðgengilegar fyrir skilgreiningu. Gildin eru skilgreind fyrir þær gerðir eiginda **frágangs húss** og **framgrills**.

| Gerð eigindar | Gildi                      |
|----------------|-----------------------------|
| Frágangur húss | Svart, Eik, Rósaviður, Hvítt |
| Framgrill    | Svart, Málmur, Hvítt         |

Næsta tafla sýnir samsetningar sem eru skilgreindar með töfluskorðunni **Litur og áferð**. Með því að nota þessa töfluskorðu er hægt skilgreina hátalara sem hefur eikaráferð og svart grill, rósaviðaráferð og hvítt grill og svo framvegis.

| Ljúk.           | Grill                       |
|----------------|-----------------------------|
| Eik            | Svart                       |
| Rósaviður       | Hvítt                       |
| Hvítt          | Svart                       |
| Hvítt          | Hvítt                       |
| Svart          | Svart                       |
| Svart          | Málmur                       | 

Hægt er að stofna kerfisskilgreindar og notandaskilgreindar taflaskorður. Nánari upplýsingar, sjá [Kerfisskilgreindar og notendaskilgreindar töfluskorður](system-defined-user-defined-table-constraints.md).

## <a name="what-syntax-should-be-used-to-write-constraints"></a>Hvaða málskipan á að nota til að skrifa skorður?
Þú verður að nota OML-málskipan (Optimization Modeling Language) þegar skorður eru skrifaðar. Kerfið notar Microsoft Solver Foundation skorðuleysara til að leysa skorðurnar.

## <a name="should-i-use-table-constraints-or-expression-constraints"></a>Á ég að nota töfluskorður eða segðarskorður?
Hægt er að nota segðarskorður eða töfluskorður, eftir því hvernig óskað er að byggja upp skorðurnar. Þú byggir upp töfluskorðu sem fylki, en segðarskorða er einstök fullyrðing. Þegar þú skilgreinir vöru, þá skiptir ekki máli hvers konar þvingun er notuð. Eftirfarandi dæmi sýnir hvaða munur er á valkostunum tveimur.  

Þegar afurð er skilgreind með því að nota eftirfarandi uppsetningar töfluskorðu eru þessar samsetningar leyfðar:

-   Afurð í litnum Svart og stærð 30 eða 50
-   Afurð í litnum Rautt og í stærð 20

### <a name="table-constraint-setup"></a>Uppsetning skilgreiningar á töfluskorðu

| Litur | Stærð |
|-------|------|
| Svart | 30   |
| Svart | 50   |
| Rautt   | 20   |

### <a name="expression-constraint-setup"></a>Uppsetning segðarskorðu

(Color == "Black" & (size == "30" | size == "50")) | (color == "Red" & size = "20")

## <a name="should-i-use-operators-or-infix-notation-when-i-write-expression-constraints"></a>Á ég nota virknitákn eða infix-tákn þegar ég að skrifa segðarskorður?
Hægt er að skrifa segðarskorðu með því að nota annaðhvort tiltæk forliðsvirknitákn eða infix-tákn. Fyrir virknitáknin **Min**, **Max** og **Abs** er ekki hægt að nota infix-tákn. Þessi virknitákn eru tekin með sem staðaðvirknitákn í flestum forritunartungumálum.

## <a name="what-operators-and-infix-notation-can-i-use-when-i-write-expression-constraints"></a>Hvaða virknitákn og infix-tákn get ég notað þegar ég að skrifa segðarskorður?
Eftirfarandi töflur sýna virknitákn og infix-tákn sem hægt er að nota þegar segðarskorða er skrifuð fyrir íhlut í afbrigðalíkani afurðar. Í dæmunum hér í fyrri töflunni er hægt að sjá hvernig á að skrifa segð með því að nota annaðhvort infix-tákn eða virknitákn.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th>Virknitákn</th>
<th>Lýsing</th>
<th>Málskipun</th>
<th>Dæmi</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Felur í sér</td>
<td>Þetta er satt ef fyrsta skilyrðið er rangt, annað skilyrðið er rétt, eða bæði.</td>
<td>Felur í sér [a, b], infix: a -: b</td>
<td><ul>
<li><strong>Operator:</strong> Bendir til[x != 0, y &gt;= 0]</li>
<li><strong>Infix-tákn:</strong> x != 0 -: y &gt;= 0</li>
</ul></td>
</tr>
<tr class="even">
<td>Og</td>
<td>Þetta er satt ef öll skilyrði eru uppfyllt. Ef skilyrði er 0 (núll), framleiðir það <strong>Rétt</strong>.</td>
<td>Og[args], infix: a &amp; b &amp; ... &amp; z</td>
<td><ul>
<li><strong>Virknitákn:</strong> Og[x == 2, y &lt;= 2]</li>
<li><strong>Infix-tákn:</strong> x == 2 &amp; y &lt;= 2</li>
</ul></td>
</tr>
<tr class="odd">
<td>Eða</td>
<td>Þetta er satt ef hvaða skilyrði er satt. Ef skilyrði er 0 (núll), framleiðir það <strong>Rangt</strong>.</td>
<td>Eða[args], infix: a | b | ... | z</td>
<td><ul>
<li><strong>Virknitákn:</strong> Or[x == 2, y &lt;= 2]</li>
<li><strong>Infix-tákn:</strong> x == 2 | y &lt;= 2</li>
</ul></td>
</tr>
<tr class="even">
<td>Plús</td>
<td>Þetta samtölur hennar skilyrði. Ef fjöldi skilyrða er 0 (núll), framleiðir það <strong>0</strong>.</td>
<td>Plús[args], infix: a + b + ... + z</td>
<td><ul>
<li><strong>Virknitákn:</strong> Plus[x, y, 2] == z</li>
<li><strong>Infix-tákn:</strong> x + y + 2 == z</li>
</ul></td>
</tr>
<tr class="odd">
<td>Mínus</td>
<td>Þetta negates hennar frumbreytu. Þetta verður að hafa nákvæmlega eitt skilyrði.</td>
<td>Mínus [expr] infix: -expr</td>
<td><ul>
<li><strong>Virknitákn:</strong> Minus[x] == y</li>
<li><strong>Infix-tákn:</strong> -x == y</li>
</ul></td>
</tr>
<tr class="even">
<td>Abs</td>
<td>Þetta tekur raungildi hennar skilyrði. Þetta verður að hafa nákvæmlega eitt skilyrði.</td>
<td>[Expr] abs</td>
<td><strong>Virknitákn:</strong> Abs[x]</td>
</tr>
<tr class="odd">
<td>Tímar</td>
<td>Þetta tekur afurðar þess skilyrða. Ef fjöldi skilyrða er 0 (núll), framleiðir það <strong>1</strong>.</td>
<td>Sinnum[args], infix: a * b * ... * z</td>
<td><ul>
<li><strong>Virknitákn:</strong> Times[x, y, 2] == z</li>
<li><strong>Infix-tákn:</strong> x * y * 2 == z</li>
</ul></td>
</tr>
<tr class="even">
<td>Styrkur</td>
<td>Þetta tekur til exponential. Þetta á við veldi frá hægri til vinstri. (Með öðrum orðum, það er hægri-tengt.) Þess vegna er, <strong>Power[a, b, c]</strong> jafnt og <strong>Power[a, Power[b, c]]</strong>. <strong>Afl</strong> er aðeins hægt að nota með jákvæða fasta sem veldisvísi.</td>
<td>Power[args], infix: a ^ b ^ ... ^ z</td>
<td><ul>
<li><strong>Virknitákn:</strong> Power[x, 2] == y</li>
<li><strong>Infix-tákn:</strong> x ^ 2 == y</li>
</ul></td>
</tr>
<tr class="odd">
<td>Hámark</td>
<td>Þetta myndar stærsta skilyrðið. Ef fjöldi skilyrða er 0 (núll), framleiðir það <strong>Óendanleiki</strong>.</td>
<td>Max [viðföng]</td>
<td><strong>Virknitákn:</strong> Max[x, y, 2] == z</td>
</tr>
<tr class="even">
<td>Lágmark</td>
<td>Þetta birtir lægstu skilyrði. Ef fjöldi skilyrða er 0 (núll), framleiðir það <strong>Óendanleiki</strong>.</td>
<td>Mín. [viðföng]</td>
<td><strong>Virknitákn:</strong> Min[x, y, 2] == z</td>
</tr>
<tr class="odd">
<td>Ekki</td>
<td>Þetta myndar röklegt inverse skilyrðis hennar. Þetta verður að hafa nákvæmlega eitt skilyrði.</td>
<td>Ekki [expr] infix: expr</td>
<td><ul>
<li><strong>Virknitákn:</strong> Ekki[x] &amp; Ekki[y == 3]</li>
<li><strong>Infix-tákn:</strong> !x!(y == 3)</li>
</ul></td>
</tr>
</tbody>
</table>

Dæmi í næstu töflu sýna hvernig á að skrifa infix-tákn.

| Infix merki    | lýsing                                                                                   |
|-------------------|-----------------------------------------------------------------------------------------------|
| x + y + z         | samlagning                                                                                      |
| x \* y \* z       | Margföldun                                                                                |
| x - y             | Frádráttur tvíundakerfis er umreiknaður eins og viðbót tvíundakerfis þar sem er neitaða aðra. |
| x ^ y ^ z         | Veldi sem hefur hægri tengslavirkni                                                   |
| !x                | Boole-ekki                                                                                   |
| x -: y            | Boole-leiðing                                                                           |
| x | y | z         | Boole- eða                                                                                    |
| x & y & z         | Boole- og                                                                                   |
| x == y == z       | Jafngildi                                                                                      |
| x != y != z       | Ákveðið                                                                                      |
| x &lt; y &lt; z   | Minna en                                                                                     |
| x &gt; y &gt; z   | Stærra en                                                                                  |
| x &lt;= y &lt;= z | Minna en eða jafnt og                                                                         |
| x &gt;= y &gt;= z | Stærra en eða jafnt og                                                                      |
| (x)               | Svigaar hnekkja sjálfgefinn forgang.                                                      |

## <a name="why-arent-my-expression-constraints-validated-correctly"></a>Af hverju eru mínar segðaskorður ekki sannprófaðar rétt?
Frátekið lykilorð er hægt að nota sem heiti leysara eigindir, íhluti eða undiríhlutir í afbrigðalíkani afurðar. Hér er listi yfir frátekin lykilorð sem ekki er hægt að nota:

-   Þak
-   Eining
-   Jafnt
-   Hæð
-   Ef
-   Minna
-   Hærri
-   Felur í sér
-   Kladdi
-   Hám.
-   Lágm
-   Mínus
-   Plús
-   Styrkur
-   Tímar
-   Rauf
-   Tegund
-   Ákvörðun
-   Markmið


<a name="see-also"></a>Sjá einnig
--------

[Stofna segð töfluskorðu (verkefnaleiðbeiningar)(tasks/add-expression-constraint-product-configuration-model.md)

[Bæta útreikningi við afbrigðalíkan afurðar (verkleiðbeiningar)](tasks/add-calculation-product-configuration-model.md)




