---
title: Sléttunarreglur skattaútreiknings
description: Í þessu efnisatriði er að finna upplýsingar um sléttunarreglur í skattaútreikningsfæribreytum í skattframtalsþjónustu.
author: kailiang
ms.date: 07/29/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.custom: ''
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 167db4d836aa754509bb28677916a30901cebbbb
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 05/04/2022
ms.locfileid: "8694175"
---
# <a name="tax-calculation-rounding-rules"></a>Sléttunarreglur skattaútreiknings

[!include [banner](../includes/banner.md)]

Í þessu efnisatriði er að finna upplýsingar um hvernig sléttunarreglur virka í skattaútreikningsfæribreytum í skattframtalsþjónustu.

> [!NOTE] 
> Þegar skattframtalsþjónustan er virkjuð eru sléttunarreglurnar á síðunum **VSK-kóði** og **VSK-flokkur** ekki virkar.

Hægt er að skoða skilgreiningu sléttunarreglna fyrir skattframtalsþjónustu í hlutanum **Sléttunarregla virðisaukaskatts** í flýtiflipanum **Útreikningur** í flipanum **Almennt** á síðunni **Færibreytur skattaútreiknings** (**Skattur** \> **Uppsetning** \> **Skattaskilgreining** \> **Færibreytur skattaútreiknings**).

[![Skilgreining sléttunarreglu á færibreytusíðu skattaútreiknings](./media/tax-calculation-parameters-calculation-1.png)](./media/tax-calculation-parameters-calculation-1.png)

Reitirnir **Sléttunarnákvæmni** og **Sléttunaraðferð** ákvarða hvernig reiknaðir reitir í innihaldinu frá skattframtalsþjónustunni eru sléttaðar.

## <a name="rounding-precision"></a>Sléttunarnákvæmni

Reitirnir **Sléttunarnákvæmni** styðja gildi sem er með allt að sex aukastafi. Til dæmis, ef þú stillir **Nákvæmni í námundun** sviði til **0.000000**, eru reiknaðar upphæðir námundaðar að sex aukastöfum og síðan sendar til Microsoft Dynamics 365 Fjármál. Ef til dæmis sléttunaraðferðin **Venjuleg sléttun** er notuð, er upphæðin **987,1234567** sléttuð í **987,123457**.

> [!NOTE]
> Finance sléttar upphæðir samkvæmt sléttunarreglum gjaldmiðils. Skattupphæðirnar sem eru sýndar og skráðar í færslum verða þar af leiðandi fyrir áhrifum frá bæði sléttunarreglum skattaútreiknings og sléttunarreglum gjaldmiðils.

## <a name="rounding-method"></a>Sléttunaraðferð

Hægt er að stilla sléttunaraðferðina fyrir skattútreikning fyrir hvern lögaðila. Í reitnum **Sléttunaraðferð** hefur þú um þrjá kosti að velja: **Venjuleg sléttun**, **Slétta niður** og **Slétta upp**.

### <a name="rounding-example"></a>Dæmi um sléttun

Eftirfarandi tafla gefur upp dæmi sem sýnir hvernig upphæðin **987,345** er sléttuð fyrir mismunandi samsetningar af sléttunarnákvæmni og sléttunaraðferðum.

<table>
<thead>
<tr>
<th rowspan="2">Sléttunaraðferð</th>
<th colspan="8">Sléttunarnákvæmni</th>
</tr>
<tr>
<th>0,00</th>
<th>0.01</th>
<th>0.10</th>
<th>1.00</th>
<th>10,00</th>
<th>0.02</th>
<th>0.05</th>
<th>0.25</th>
</tr>
</thead>
<tbody>
<tr>
<td>Venjulegt</td>
<td>987.35</td>
<td>987.35</td>
<td>987.30</td>
<td>987.00</td>
<td>990.00</td>
<td>987.34</td>
<td>987.35</td>
<td>987.25</td>
</tr>
<tr>
<td>Slétta niður</td>
<td>987.00</td>
<td>987.34</td>
<td>987.30</td>
<td>987.00</td>
<td>980.00</td>
<td>987.34</td>
<td>987.30</td>
<td>987.25</td>
</tr>
<tr>
<td>Slétta upp</td>
<td>988.00</td>
<td>987.35</td>
<td>987.40</td>
<td>988.00</td>
<td>990.00</td>
<td>987.36</td>
<td>987.35</td>
<td>987.50</td>
</tr>
</tbody>
</table>

Hægt er að skilgreina útreikning og sléttunarrök skattupphæða samkvæmt skattareglum.

## <a name="rounding-by"></a>Sléttað eftir 

Í reitnum **Sléttað eftir** skal velja sléttunarleiðina sem gildir um skattana. Eftirtaldir valkostir eru í boði:

- **Skattkóðar** – Sléttaðu skattupphæðina í hverjum skattkóða.
- **Samsetningar skattkóða** – Sléttaðu skattupphæðina í samsetningu skattkóða í línunni.

## <a name="calculation-method"></a>Útreikningsaðferð

Í reitnum **Útreikningsaðferð** skal velja hvort skattar á reikningum séu reiknaðir fyrir hverja línu eða allar línur. Eftirtaldir valkostir eru í boði:

- **Lína** – Reikna skattupphæðina eina línu í einu. Skattfjárhæð hverrar línu hefur engin áhrif á skattfjárhæð annarra lína.
- **Samtals** – Reiknaðu skattfjárhæðina á allar línurnar í einu skjali.

### <a name="rounding-calculation-example"></a>Dæmi um útreikning sléttunar

Þetta dæmi sýnir mismunandi útreikninga sem hægt er að gera fyrir einn reikning, fyrir mismunandi samsetningar af gildum fyrir **Sléttað eftir** og **Útreikningsaðferð**. Í þessu dæmi er eftirfarandi uppsetning til staðar:

- Reikningurinn er með fjórum línum.
- Það eru tveir skattkóðar: **VSK1** (10 prósent) og **VSK2** (10 prósent).
- Sléttunarnákvæmnin er stillt á **0,01**.
- Sléttunaraðferðin er stillt á **Slétta upp**.

#### <a name="rounding-by--tax-codes-and-calculation-method--line"></a>Sléttað eftir = Skattkóðar og útreikningsaðferð = Lína

| Línunúmer | Nettóupphæð línu | Ákvarðaðir skattkóðar | Skattfjárhæð fyrir sléttun | Sléttuð skattupphæð |
|-------------|-----------------|----------------------|----------------------------|--------------------|
| 1           | 11.11           | VAT1                 | 1.111                      | 1.12               |
| 2           | 22.22           | VAT1; VAT2           | 2,222; 2,222               | 2,23; 2,23         |
| 3           | 33.33           | VAT1                 | 3.333                      | 3.34               |
| 4           | 44.44           | VAT1; VAT2           | 4,444; 4;444               | 4,45; 4,45         |

#### <a name="rounding-by--tax-code-combinations-and-calculation-method--line"></a>Sléttað eftir = Samsetningar skattkóða og útreikningsaðferð = Lína

| Línunúmer | Nettóupphæð línu | Ákvarðaðir skattkóðar | Skattfjárhæð fyrir sléttun | Sléttuð skattupphæð |
|-------------|-----------------|----------------------|----------------------------|--------------------|
| 1           | 11.11           | VAT1                 | 1.111                      | 1.12               |
| 2\*         | 22.22           | VAT1; VAT2           | 2,222; 2,222               | 2,23; 2,22         |
| 3           | 33.33           | VAT1                 | 3.333                      | 3.34               |
| 4\*\*       | 44.44           | VAT1; VAT2           | 4,444; 4;444               | 4,45; 4,44         |

\* Lína 2 = Slétta\[22,22 × (10 prósent + 10 prósent)\] = 2,23 + 2,22

\*\* Lína 4 = Slétta\[44,44 × (10 prósent + 10 prósent)\] = 4,45 + 4,44

#### <a name="rounding-by--tax-codes-and-calculation-method--total"></a>Sléttað eftir = Skattkóðar og útreikningsaðferð = Samtala

| Línunúmer | Nettóupphæð línu | Ákvarðaðir skattkóðar | Skattfjárhæð fyrir sléttun | Sléttuð skattupphæð |
|-------------|-----------------|----------------------|----------------------------|--------------------|
| 1           | 11.11           | VAT1\*               | 1.111                      | 1.12               |
| 2           | 22.22           | VAT1\*; VAT2\*\*     | 2,222; 2,222               | 2,22; 2,23         |
| 3           | 33.33           | VAT1\*               | 3.333                      | 3.33               |
| 4           | 44.44           | VAT1\*; VAT2\*\*     | 4,444; 4;444               | 4,44; 4,44         |

\* VSK1(lína 1, lína 2, lína 3, lína 4) = Slétta\[(11,11 + 22,22 + 33,33 + 44,44) × 10 prósent\] = 1,12 + 2,22 + 3,33 + 4,44

\*\* VSK2(lína 2, lína4) = Slétta\[(22,22 + 44,44) × 10 prósent\] = 2,23 + 4,44

#### <a name="rounding-by--tax-code-combinations-and-calculation-method--total"></a>Sléttað eftir = Samsetningar skattkóða og útreikningsaðferð = Samtala

| Línunúmer | Nettóupphæð línu | Ákvarðaðir skattkóðar | Skattfjárhæð fyrir sléttun | Sléttuð skattupphæð |
|-------------|-----------------|----------------------|----------------------------|--------------------|
| 1\*         | 11.11           | VAT1                 | 1.111                      | 1.12               |
| 2\*\*       | 22.22           | VAT1; VAT2           | 2,222; 2,222               | 2,23; 2,22         |
| 3\*         | 33.33           | VAT1                 | 3.333                      | 3.33               |
| 4\*\*       | 44.44           | VAT1; VAT2           | 4,444; 4;444               | 4,44; 4,45         |

\* Lína 1, lína 3 = Slétta\[(11,11 + 33,33) × 10 prósent\] = 1,12 + 3,33

\*\* Lína 2, lína 4 = Slétta\[(22,22 + 44,44) × (10 prósent + 10 prósent)\] = 2,23 + 2,22 + 4,44 + 4,45

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
