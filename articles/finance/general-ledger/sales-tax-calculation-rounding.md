---
title: Útreikningur söluskatts og námundun
description: Þessi grein veitir yfirlit yfir söluskattsútreikning og námundun og útskýrir færibreytur söluskattsútreiknings og námundunaruppsetningar.
author: wangchen
ms.date: 06/01/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: kfend
ms.custom:
- "13111"
- intro-internal
ms.assetid: fe5fdc7f-9834-49fb-a611-1dd9c289619d
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2022-05-31
ms.dyn365.ops.version: AX 10.0.28
ms.openlocfilehash: aa3564f0fcf4a958637ba4a5cdcc497bffc50000
ms.sourcegitcommit: 8b716849707ec96d1cb4cac85b9e782dc25f5a70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/07/2022
ms.locfileid: "8939234"
---
# <a name="sales-tax-calculation-and-rounding"></a>Útreikningur söluskatts og námundun

[!include [banner](../includes/banner.md)]

Þessi grein veitir yfirlit yfir útreikning söluskatts og námundun Microsoft Dynamics 365 Fjármál. Það útskýrir einnig færibreyturnar sem eru notaðar í uppsetningunni fyrir útreikning á söluskatti og námundun og hvernig þær færibreytur vinna saman.

## <a name="parameters"></a>Færibreytur

Nokkrar færibreytur stjórna útreikningi söluskatts og námundun:

- **Reikniaðferð** – Þessi færibreyta er stillt á **Fjárhagsfæribreytur** síðu og skilgreinir hvort skattstofnfjárhæð er reiknuð á skjal eða línu. Ef **Jaðargrunnur** færibreyta fyrir vsk kóða er stillt á **Nettóupphæð reikningsstöðu**, skattstofnsupphæð er alltaf reiknuð út fyrir hvert skjal, óháð stillingu þessarar færibreytu.
- **Hringur framhjá** – Þessi færibreyta er stillt fyrir vsk-flokkinn og skilgreinir hvort vskupphæðin er námunduð á vsk-kóða eða vsk-kóðasamsetningu.
- **Uppruni** – Þessi færibreyta er stillt fyrir vsk-kóðann og skilgreinir hvernig skattupphæðin er reiknuð út. Fyrir frekari upplýsingar, sjá [Útreikningsaðferðir söluskatts í reitnum Uppruni](sales-tax-calculation-methods-origin-field.md).
- **Jaðargrunnur** – Þessi færibreyta er stillt fyrir VSK-kóðann og ákvarðar hvaða upphæð er notuð til að velja viðeigandi skatthlutföll á **Vöruskattsnúmer gildi** síðu. Nánari upplýsingar er að finna í [Skatthlutfall virðisaukaskatts á grundvelli Jaðargrunns og Útreikningsaðferðar](marginal-base-field.md)
- **Söluskattssléttunarregla** – Þessi færibreyta er stillt fyrir virðisaukaskattskóðann og skilgreinir hvernig ákvörðuð virðisaukaskattsupphæð er námunduð, þar á meðal námundunarnákvæmni og námundunaraðferð.

Afgangurinn af þessari grein sýnir nokkur dæmigerð dæmi um útreikning söluskatts og námundun sem notar samsetningu af fyrri færibreytum.

## <a name="scenario-for-the-examples"></a>Sviðsmynd fyrir dæmin

- Í skattskjalinu eru tvær línur og er stofnfjárhæð hverrar línu 42,42.
- Tveir VSK-kóðar eru skilgreindir fyrir hverja línu: VSK-kóði 1 og VSK-kóði 2.
- Skatthlutfall bæði skattnúmers 1 og skattnúmers 2 er 10 prósent.
- Verðið er án skatts.
- Nákvæmni námundunar er 0,01.
- Námundunaraðferðin er **Röð upp**.

## <a name="example-1"></a>Dæmi 1

### <a name="parameter-values"></a>Færigildi

| Útreikningsaðferð | Sléttað eftir    | Uppruni                   | Jaðargrunnur       |
| ------------------ | -------------- | ------------------------ | ------------------- |
| Lína               | VSK-kóði | Prósenta af nettóupphæð | Nettóupphæð á línu |

### <a name="calculation-and-rounding-behavior"></a>Útreiknings- og námundunarhegðun

| Línunúmer | VSK-kóði | Uppruni upphæðar | Upphæð virðisaukaskatts |
| ------------| ---------------| --------------| -----------------|
| 1           | Kóði 1         | 42,42         | 4,25             |
| 1           | Kóði 2         | 42,42         | 4,25             |
| 2           | Kóði 1         | 42,42         | 4,25             |
| 2           | Kóði 2         | 42,42         | 4,25             |

Skattstofnfjárhæð er reiknuð fyrir hverja línu:

- **Lína 1:** 42,42
- **Lína 2:** 42,42

Skattupphæðin er reiknuð út eftir vsk-kóða:

- **Lína 1:**

    - Skattupphæð fyrir vsk kóða 1 = 42,42&times; 10 prósent = 4,242
    - Skattupphæð fyrir vsk kóða 2 = 42,42&times; 10 prósent = 4,242

- **Lína 2:**

    - Skattupphæð fyrir vsk kóða 1 = 42,42&times; 10 prósent = 4,242
    - Skattupphæð fyrir vsk kóða 2 = 42,42&times; 10 prósent = 4,242

Skattupphæðin er námunduð eftir vsk-kóða:

- **Lína 1:**

    - Námunduð skattupphæð fyrir vsk kóða 1 = 4,25
    - Námunduð skattupphæð fyrir vsk kóða 2 = 4,25

- **Lína 2:**

    - Námunduð skattupphæð fyrir vsk kóða 1 = 4,25
    - Námunduð skattupphæð fyrir vsk kóða 2 = 4,25

## <a name="example-2"></a>Dæmi 2

### <a name="parameter-values"></a>Færigildi

| Útreikningsaðferð | Sléttað eftir    | Uppruni                   | Jaðargrunnur                 |
| ------------------ | -------------- | ------------------------ | ----------------------------- |
| Lína/Total         | VSK-kóði | Prósenta af nettóupphæð | Nettóupphæð af reikningsstöðu |

### <a name="calculation-and-rounding-behavior"></a>Útreiknings- og námundunarhegðun

| Línunúmer | VSK-kóði | Uppruni upphæðar | Upphæð virðisaukaskatts |
| ----------- | -------------- | ------------- | ---------------- |
| 1           | Kóði 1         | 42,42         | 4,25             |
| 1           | Kóði 2         | 42,42         | 4,25             |
| 2           | Kóði 1         | 42,42         | 4,24             |
| 2           | Kóði 2         | 42,42         | 4,24             |

Skattstofnfjárhæð er reiknuð fyrir hvert skjal:

- Skattstofnupphæð = 42,42 + 42,42 = 84,84

Skattupphæðin er reiknuð út eftir vsk-kóða:

- Skattupphæð fyrir vsk kóða 1 = 84,84&times; 10 prósent = 8.484
- Skattupphæð fyrir vsk kóða 2 = 84,84&times; 10 prósent = 8.484

Skattupphæðin er námunduð eftir vsk-kóða:

- Námunduð skattupphæð fyrir vsk kóða 1 = 8,49
- Námunduð skattupphæð fyrir vsk kóða 2 = 8,49

Ámundaðri skattupphæð er úthlutað á hverja línu fyrir hvern söluskattskóða:

- Úthlutaðu ávölu skattupphæðinni fyrir VSK-kóða 1 (8.49) í línu 1 (4.25) og línu 2 (4.24).
- Úthlutaðu ávölu skattupphæðinni fyrir vsk kóða 2 (8.49) í línu 1 (4.25) og línu 2 (4.24).

## <a name="example-3"></a>Dæmi 3

### <a name="parameter-values"></a>Færigildi

| Útreikningsaðferð | Sléttað eftir    | Uppruni                              | Jaðargrunnur       |
| ------------------ | -------------- | ----------------------------------- | ------------------- |
| Lína               | VSK-kóði | Reiknuð prósenta af nettóupphæð | Nettóupphæð á línu |

### <a name="calculation-and-rounding-behavior"></a>Útreiknings- og námundunarhegðun

| Línunúmer | VSK-kóði | Uppruni upphæðar | Upphæð virðisaukaskatts |
| ----------- | -------------- | ------------- | ---------------- |
| 1           | Kóði 1         | 42,42         | 4,72             |
| 1           | Kóði 2         | 42,42         | 4,72             |
| 2           | Kóði 1         | 42,42         | 4,72             |
| 2           | Kóði 2         | 42,42         | 4,72             |

Skattstofnfjárhæð er reiknuð fyrir hverja línu:

- **Lína 1:** 42,42
- **Lína 2:** 42,42

Skattupphæðin er reiknuð út eftir vsk-kóða:

- **Lína 1:**

    - Skattupphæð fyrir vsk kóða 1 = 42,42&times; 10 prósent&divide; (1 – 10 prósent) = 4,7133
    - Skattupphæð fyrir vsk kóða 2 = 42,42&times; 10 prósent&divide; (1 – 10 prósent) = 4,7133

- **Lína 2:**

    - Skattupphæð fyrir vsk kóða 1 = 42,42&times; 10 prósent&divide; (1 – 10 prósent) = 4,7133
    - Skattupphæð fyrir vsk kóða 2 = 42,42&times; 10 prósent&divide; (1 – 10 prósent) = 4,7133

Skattupphæðin er námunduð eftir vsk-kóða:

- **Lína 1:**

    - Námunduð skattupphæð fyrir vsk kóða 1 = 4,72
    - Námunduð skattupphæð fyrir vsk kóða 2 = 4,72

- **Lína 2:**

    - Námunduð skattupphæð fyrir vsk kóða 1 = 4,72
    - Námunduð skattupphæð fyrir vsk kóða 2 = 4,72

## <a name="example-4"></a>Dæmi 4

### <a name="parameter-values"></a>Færigildi

| Útreikningsaðferð | Sléttað eftir    | Uppruni                              | Jaðargrunnur                 |
| ------------------ | -------------- | ----------------------------------- | ----------------------------- |
| Lína/Total         | VSK-kóði | Reiknuð prósenta af nettóupphæð | Nettóupphæð af reikningsstöðu |

### <a name="calculation-and-rounding-behavior"></a>Útreiknings- og námundunarhegðun

| Línunúmer | VSK-kóði | Uppruni upphæðar | Upphæð virðisaukaskatts |
| ----------- | -------------- | ------------- | ---------------- |
| 1           | Kóði 1         | 42,42         | 4,72             |
| 1           | Kóði 2         | 42,42         | 4,72             |
| 2           | Kóði 1         | 42,42         | 4,71             |
| 2           | Kóði 2         | 42,42         | 4,71             |

Skattstofnfjárhæð er reiknuð fyrir hvert skjal:

- Skattstofnupphæð = 42,42 + 42,42 = 84,84

Skattupphæðin er reiknuð út eftir vsk-kóða:

- Skattupphæð fyrir vsk kóða 1 = 84,84&times; 10 prósent&divide; (1 – 10 prósent) = 9,4267
- Skattupphæð fyrir vsk kóða 2 = 84,84&times; 10 prósent&divide; (1 – 10 prósent) = 9,4267

Skattupphæðin er námunduð eftir vsk-kóða:

- Námunduð skattupphæð fyrir vsk kóða 1 = 9,43
- Námunduð skattupphæð fyrir vsk kóða 2 = 9,43

Ámundaðri skattupphæð er úthlutað á hverja línu fyrir hvern söluskattskóða:

- Úthlutaðu skattupphæðinni fyrir vsk kóða 1 (9.43) í línu 1 (4.72) og línu 2 (4.71).
- Úthlutaðu skattupphæðinni fyrir vsk kóða 2 (9.43) í línu 1 (4.72) og línu 2 (4.71).

## <a name="example-5"></a>Dæmi 5

### <a name="parameter-values"></a>Færigildi

| Útreikningsaðferð | Sléttað eftir                | Uppruni                   | Jaðargrunnur       |
| ------------------ | -------------------------- | ------------------------ | ------------------- |
| Lína               | VSK-kóðasamsetning | Prósenta af nettóupphæð | Nettóupphæð á línu |

### <a name="calculation-and-rounding-behavior"></a>Útreiknings- og námundunarhegðun

| Línunúmer | VSK-kóði | Uppruni upphæðar | Upphæð virðisaukaskatts |
| ----------- | -------------- | ------------- | ---------------- |
| 1           | Kóði 1         | 42,42         | 4,25             |
| 1           | Kóði 2         | 42,42         | 4,24             |
| 2           | Kóði 1         | 42,42         | 4,24             |
| 2           | Kóði 2         | 42,42         | 4,24             |

Skattstofnfjárhæð er reiknuð fyrir hverja línu:

- **Lína 1:** 42,42
- **Lína 2:** 42,42

Skattupphæðin er reiknuð út eftir vsk-kóða:

- **Lína 1:**

    - Skattupphæð fyrir vsk kóða 1 = 42,42&times; 10 prósent = 4,242
    - Skattupphæð fyrir vsk kóða 2 = 42,42&times; 10 prósent = 4,242

- **Lína 2:**

    - Skattupphæð fyrir vsk kóða 1 = 42,42&times; 10 prósent = 4,242
    - Skattupphæð fyrir vsk kóða 2 = 42,42&times; 10 prósent = 4,242

Skattupphæðin er námunduð eftir samsetningu vsk kóða:

- Heildarupphæð söluskatts = 4.242 + 4.242 + 4.242 + 4.242 = 16.968, sem er námundað upp í 16.97

Ámundaðri skattupphæð er úthlutað á hverja línu fyrir hvern söluskattskóða:

- Úthlutaðu söluskattsupphæðinni (16,97) á línu 1 og línu 2:

    - **Lína 1:**

        - Skattupphæð fyrir vsk kóða 1 = 4,25
        - Skattupphæð fyrir vsk kóða 2 = 4.24

    - **Lína 2:**

        - Skattupphæð fyrir vsk kóða 1 = 4.24
        - Skattupphæð fyrir vsk kóða 2 = 4.24

## <a name="example-6"></a>Dæmi 6

### <a name="parameter-values"></a>Færigildi

| Útreikningsaðferð | Sléttað eftir                | Uppruni                   | Jaðargrunnur                 |
| ------------------ | -------------------------- | ------------------------ | ----------------------------- |
| Lína/Total         | VSK-kóðasamsetning | Prósenta af nettóupphæð | Nettóupphæð af reikningsstöðu |

### <a name="calculation-and-rounding-behavior"></a>Útreiknings- og námundunarhegðun

| Línunúmer | VSK-kóði | Uppruni upphæðar | Upphæð virðisaukaskatts |
| ----------- | -------------- | ------------- | ---------------- |
| 1           | Kóði 1         | 42,42         | 4,25             |
| 1           | Kóði 2         | 42,42         | 4,24             |
| 2           | Kóði 1         | 42,42         | 4,24             |
| 2           | Kóði 2         | 42,42         | 4,24             |

Skattstofnfjárhæð er reiknuð fyrir hvert skjal:

- Skattstofnupphæð = 42,42 + 42,42 = 84,84

Skattupphæðin er reiknuð út eftir vsk-kóða:

- Skattupphæð fyrir vsk kóða 1 = 84,84&times; 10 prósent = 8.484
- Skattupphæð fyrir vsk kóða 2 = 84,84&times; 10 prósent = 8.484

Skattupphæðin er námunduð eftir samsetningu vsk kóða:

- Heildarupphæð söluskatts = 8.484 + 8.484 = 16.968, sem er námundað upp í 16.97

Ámundaðri skattupphæð er úthlutað á hverja línu fyrir hvern söluskattskóða:

- Úthlutaðu söluskattsupphæðinni (16,97) á línu 1 og línu 2:

    - **Lína 1:**

        - Skattupphæð fyrir vsk kóða 1 = 4,25
        - Skattupphæð fyrir vsk kóða 2 = 4.24

    - **Lína 2:**

        - Skattupphæð fyrir vsk kóða 1 = 4.24
        - Skattupphæð fyrir vsk kóða 2 = 4.24

## <a name="example-7"></a>Dæmi 7

### <a name="parameter-values"></a>Færigildi

| Útreikningsaðferð | Sléttað eftir                | Uppruni                              | Jaðargrunnur       |
| ------------------ | -------------------------- | ----------------------------------- | ------------------- |
| Lína               | VSK-kóðasamsetning | Reiknuð prósenta af nettóupphæð | Nettóupphæð á línu |

### <a name="calculation-and-rounding-behavior"></a>Útreiknings- og námundunarhegðun

| Línunúmer | VSK-kóði | Uppruni upphæðar | Upphæð virðisaukaskatts |
| ----------- | -------------- | ------------- | ---------------- |
| 1           | Kóði 1         | 42,42         | 4,72             |
| 1           | Kóði 2         | 42,42         | 4,71             |
| 2           | Kóði 1         | 42,42         | 4,71             |
| 2           | Kóði 2         | 42,42         | 4,72             |

Skattstofnfjárhæð er reiknuð fyrir hverja línu:

- **Lína 1:** 42,42
- **Lína 2:** 42,42

Skattupphæðin er reiknuð út eftir vsk-kóða:

- **Lína 1:**

    - Skattupphæð fyrir vsk kóða 1 = 42,42&times; 10 prósent&divide; (1 – 10 prósent) = 4,7133
    - Skattupphæð fyrir vsk kóða 2 = 42,42&times; 10 prósent&divide; (1 – 10 prósent) = 4,7133

- **Lína 2:**

    - Skattupphæð fyrir vsk kóða 1 = 42,42&times; 10 prósent&divide; (1 – 10 prósent) = 4,7133
    - Skattupphæð fyrir vsk kóða 2 = 42,42&times; 10 prósent&divide; (1 – 10 prósent) = 4,7133

Skattupphæðin er námunduð eftir samsetningu vsk kóða:

- Heildarupphæð söluskatts = 4,7133 + 4,7133 + 4,7133 + 4,7133 = 18,8532, sem er námundað upp í 18,86

Ámundaðri skattupphæð er úthlutað á hverja línu fyrir hvern söluskattskóða:

- Úthlutaðu söluskattsupphæðinni (18,86) á línu 1 og línu 2:

    - **Lína 1:**

        - Skattupphæð fyrir vsk kóða 1 = 4,72
        - Skattupphæð fyrir vsk kóða 2 = 4,71

    - **Lína 2:**

        - Skattupphæð fyrir vsk kóða 1 = 4,71
        - Skattupphæð fyrir vsk kóða 2 = 4,72

## <a name="example-8"></a>Dæmi 8

### <a name="parameter-values"></a>Færigildi

| Útreikningsaðferð | Sléttað eftir                | Uppruni                              | Jaðargrunnur                 |
| ------------------ | -------------------------- | ----------------------------------- | ----------------------------- |
| Lína/Total         | VSK-kóðasamsetning | Reiknuð prósenta af nettóupphæð | Nettóupphæð af reikningsstöðu |

### <a name="calculation-and-rounding-behavior"></a>Útreiknings- og námundunarhegðun

| Línunúmer | VSK-kóði | Uppruni upphæðar | Upphæð virðisaukaskatts |
| ----------- | -------------- | ------------- | ---------------- |
| 1           | Kóði 1         | 42,42         | 4,72             |
| 1           | Kóði 2         | 42,42         | 4,71             |
| 2           | Kóði 1         | 42,42         | 4,71             |
| 2           | Kóði 2         | 42,42         | 4,72             |

Skattstofnfjárhæð er reiknuð fyrir hvert skjal:

- Skattstofnupphæð = 42,42 + 42,42 = 84,84

Skattupphæðin er reiknuð út eftir vsk-kóða:

- Skattupphæð fyrir vsk kóða 1 = 84,84&times; 10 prósent&divide; (1 – 10 prósent) = 9,4267
- Skattupphæð fyrir vsk kóða 2 = 84,84&times; 10 prósent&divide; (1 – 10 prósent) = 9,4267

Skattupphæðin er námunduð eftir samsetningu vsk kóða:

- Heildarupphæð söluskatts = 9,4267 + 9,4267 = 18,8534, sem er námundað upp í 18,86

Ámundaðri skattupphæð er úthlutað á hverja línu fyrir hvern söluskattskóða:

- Úthlutaðu söluskattsupphæðinni (18,86) á línu 1 og línu 2:

    - **Lína 1:**

        - Skattupphæð fyrir vsk kóða 1 = 4,72
        - Skattupphæð fyrir vsk kóða 2 = 4,71

    - **Lína 2:**

        - Skattupphæð fyrir vsk kóða 1 = 4,71
        - Skattupphæð fyrir vsk kóða 2 = 4,72

## <a name="additional-resources"></a>Frekari upplýsingar

- [Útreikningsaðferðir VSK í upprunareitnum](sales-tax-calculation-methods-origin-field.md)
- [Virðisaukaskattur byggður á jaðargrunns- og útreikningsaðferðum](marginal-base-field.md)
- [Valkostir heildarupphæðar og tímabilsútreikninga fyrir VSK-kóða](whole-amount-interval-options-sales-tax-codes.md)
