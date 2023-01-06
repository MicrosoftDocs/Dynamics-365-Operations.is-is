---
title: VSK-útreikningur og sléttun
description: Í þessari grein er að finna yfirlit yfir útreikning VSK og sléttun og útskýringar á færibreytum í útreikningi VSK og uppsetningu sléttunar.
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
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/07/2022
ms.locfileid: "8939234"
---
# <a name="sales-tax-calculation-and-rounding"></a>VSK-útreikningur og sléttun

[!include [banner](../includes/banner.md)]

Í þessari grein er að finna yfirlit yfir söluskattsútreikning og sléttun í Microsoft Dynamics 365 Finance. Einnig er útskýrt hvaða breytur eru notaðar við uppsetningu á útreikningi á söluskatti og námundun og hvernig þær breytur vinna saman.

## <a name="parameters"></a>Færibreytur

Nokkrar færibreytur stjórna VSK-útreikningi og sléttun:

- **Útreikningsaðferð** – Þessi færibreyta er sett upp á síðunni **Færibreytur fjárhags** og skilgreinir hvort skattgrunnupphæðin er reiknuð á hvert skjal eða hverja línu. Ef **Jaðargrunnur** færibreytan fyrir VSK-kóðann er stillt á **Nettó upphæð af reikningsstöðu** er alltaf reiknuð skattgrunnupphæð fyrir hvert skjal, óháð stillingu þessarar færibreytu.
- **Sléttað eftir** – Þessi færibreyta er stillt fyrir VSK-flokkinn og skilgreinir hvort skattupphæðin er námunduð að VSK-kóða eða samsetningu VSK-kóða.
- **Uppruni** – Þessi breyta er sett fyrir söluskattskóðann og skilgreinir hvernig skattupphæðin er reiknuð. Frekari upplýsingar eru í [Útreikningsaðferðir virðisaukaskatts í reitnum Uppruni](sales-tax-calculation-methods-origin-field.md).
- **Jaðargrunnur** – Þessi færibreyta er stillt fyrir VSK-kóðann og ákvarðar hvaða upphæð er notuð til að velja viðeigandi skatthlutföll á síðunni **Gildi VSK-kóða**. Nánari upplýsingar er að finna í [Skatthlutfall virðisaukaskatts á grundvelli Jaðargrunns og Útreikningsaðferðar](marginal-base-field.md)
- **Sléttunarregla virðisaukaskatts** – Þessi færibreyta er stillt fyrir VSK-kóðann og skilgreinir hvernig upphæð virðisaukaskatts er reiknuð, þ.m.t. sléttunarnákvæmni og sléttunaraðferð.

Í þessari grein eru sýnd nokkur dæmi um útreikning á söluskatti og námundun sem nota samblöndu af framangreindum breytum.

## <a name="scenario-for-the-examples"></a>Sviðsmynd fyrir dæmin

- Það eru tvær línur í skattskyldu skjalinu, og skattstofn upphæð fyrir hverja línu er 42,42.
- Skilgreindir eru tveir skattkóðar fyrir hverja línu: söluskattur 1 og söluskattur 2.
- Skatthlutfall bæði skattkóða 1 og skattkóða 2 er 10 prósent.
- Verðið er án skatts.
- Sléttunarnákvæmnin er 0,01.
- Námundunaraðferðin er **Námunda**.

## <a name="example-1"></a>Dæmi 1

### <a name="parameter-values"></a>Gildi færibreytu

| Útreikningsaðferð | Sléttað eftir    | Uppruni                   | Jaðargrunnur       |
| ------------------ | -------------- | ------------------------ | ------------------- |
| Lína               | VSK-kóði | Prósenta af nettóupphæð | Nettóupphæð á línu |

### <a name="calculation-and-rounding-behavior"></a>Útreiknings- og sléttunarhegðun

| Línunúmer | VSK-kóði | Uppruni upphæðar | Upphæð virðisaukaskatts |
| ------------| ---------------| --------------| -----------------|
| 1           | Kóði 1         | 42,42         | 4,25             |
| 1           | Kóði 2         | 42,42         | 4,25             |
| 2           | Kóði 1         | 42,42         | 4,25             |
| 2           | Kóði 2         | 42,42         | 4,25             |

Grunnfjárhæð skatts er reiknuð fyrir hverja línu:

- **1. lína:** 42,42
- **Lína 2:** 42,42

Skattupphæðin er reiknuð út eftir skattakóða:

- **Lína 1:**

    - Skattaupphæð fyrir VSK-kóða 1 = 42,42 &times; 10 prósent = 4,242
    - Skattaupphæð fyrir VSK-kóða 2 = 42,42 &times; 10 prósent = 4,242

- **Lína 2:**

    - Skattaupphæð fyrir VSK-kóða 1 = 42,42 &times; 10 prósent = 4,242
    - Skattaupphæð fyrir VSK-kóða 2 = 42,42 &times; 10 prósent = 4,242

Skattupphæðin er námunduð eftir skattakóða:

- **Lína 1:**

    - Sléttuð skattaupphæð fyrir VSK-kóða 1 = 4,25
    - Sléttuð skattaupphæð fyrir VSK-kóða 2 = 4,25

- **Lína 2:**

    - Sléttuð skattaupphæð fyrir VSK-kóða 1 = 4,25
    - Sléttuð skattaupphæð fyrir VSK-kóða 2 = 4,25

## <a name="example-2"></a>Dæmi 2

### <a name="parameter-values"></a>Gildi færibreytu

| Útreikningsaðferð | Sléttað eftir    | Uppruni                   | Jaðargrunnur                 |
| ------------------ | -------------- | ------------------------ | ----------------------------- |
| Lína/Samtals         | VSK-kóði | Prósenta af nettóupphæð | Nettóupphæð af reikningsstöðu |

### <a name="calculation-and-rounding-behavior"></a>Útreiknings- og sléttunarhegðun

| Línunúmer | VSK-kóði | Uppruni upphæðar | Upphæð virðisaukaskatts |
| ----------- | -------------- | ------------- | ---------------- |
| 1           | Kóði 1         | 42,42         | 4,25             |
| 1           | Kóði 2         | 42,42         | 4,25             |
| 2           | Kóði 1         | 42,42         | 4,24             |
| 2           | Kóði 2         | 42,42         | 4,24             |

Grunnfjárhæð skatts er reiknuð fyrir hvert skjal:

- Grunnupphæð skatts = 42,42 + 42,42 = 84,84

Skattupphæðin er reiknuð út eftir skattakóða:

- Skattaupphæð fyrir VSK-kóða 1 = 84,84 &times; 10 prósent = 8,484
- Skattaupphæð fyrir VSK-kóða 2 = 84,84 &times; 10 prósent = 8,484

Skattupphæðin er námunduð eftir skattakóða:

- Sléttuð skattaupphæð fyrir VSK-kóða 1 = 8,49
- Sléttuð skattaupphæð fyrir VSK-kóða 2 = 8,49

Sléttaðri skattupphæð er úthlutað á hverja línu eftir VSK-kóða:

- Úthluta skal námundaðri skattfjárhæð fyrir söluskattskóða 1 (8,49) í línu 1 (4,25) og línu 2 (4,24).
- Úthluta skal námundaðri skattfjárhæð fyrir söluskattskóða 2 (8,49) í línu 1 (4,25) og línu 2 (4,24).

## <a name="example-3"></a>Dæmi 3

### <a name="parameter-values"></a>Gildi færibreytu

| Útreikningsaðferð | Sléttað eftir    | Uppruni                              | Jaðargrunnur       |
| ------------------ | -------------- | ----------------------------------- | ------------------- |
| Lína               | VSK-kóði | Reiknuð prósenta af nettóupphæð | Nettóupphæð á línu |

### <a name="calculation-and-rounding-behavior"></a>Útreiknings- og sléttunarhegðun

| Línunúmer | VSK-kóði | Uppruni upphæðar | Upphæð virðisaukaskatts |
| ----------- | -------------- | ------------- | ---------------- |
| 1           | Kóði 1         | 42,42         | 4,72             |
| 1           | Kóði 2         | 42,42         | 4,72             |
| 2           | Kóði 1         | 42,42         | 4,72             |
| 2           | Kóði 2         | 42,42         | 4,72             |

Grunnfjárhæð skatts er reiknuð fyrir hverja línu:

- **1. lína:** 42,42
- **Lína 2:** 42,42

Skattupphæðin er reiknuð út eftir skattakóða:

- **Lína 1:**

    - Skattaupphæð fyrir VSK-kóða 1 = 42,42 &times; 10 prósent &divide; (1 – 10 prósent) 4,7133
    - Skattaupphæð fyrir VSK-kóða 2 = 42,42 &times; 10 prósent &divide; (1 – 10 prósent) 4,7133

- **Lína 2:**

    - Skattaupphæð fyrir VSK-kóða 1 = 42,42 &times; 10 prósent &divide; (1 – 10 prósent) 4,7133
    - Skattaupphæð fyrir VSK-kóða 2 = 42,42 &times; 10 prósent &divide; (1 – 10 prósent) 4,7133

Skattupphæðin er námunduð eftir skattakóða:

- **Lína 1:**

    - Sléttuð skattaupphæð fyrir VSK-kóða 1 = 4,72
    - Sléttuð skattaupphæð fyrir VSK-kóða 2 = 4,72

- **Lína 2:**

    - Sléttuð skattaupphæð fyrir VSK-kóða 1 = 4,72
    - Sléttuð skattaupphæð fyrir VSK-kóða 2 = 4,72

## <a name="example-4"></a>Dæmi 4

### <a name="parameter-values"></a>Gildi færibreytu

| Útreikningsaðferð | Sléttað eftir    | Uppruni                              | Jaðargrunnur                 |
| ------------------ | -------------- | ----------------------------------- | ----------------------------- |
| Lína/Samtals         | VSK-kóði | Reiknuð prósenta af nettóupphæð | Nettóupphæð af reikningsstöðu |

### <a name="calculation-and-rounding-behavior"></a>Útreiknings- og sléttunarhegðun

| Línunúmer | VSK-kóði | Uppruni upphæðar | Upphæð virðisaukaskatts |
| ----------- | -------------- | ------------- | ---------------- |
| 1           | Kóði 1         | 42,42         | 4,72             |
| 1           | Kóði 2         | 42,42         | 4,72             |
| 2           | Kóði 1         | 42,42         | 4,71             |
| 2           | Kóði 2         | 42,42         | 4,71             |

Grunnfjárhæð skatts er reiknuð fyrir hvert skjal:

- Grunnupphæð skatts = 42,42 + 42,42 = 84,84

Skattupphæðin er reiknuð út eftir skattakóða:

- Skattaupphæð fyrir VSK-kóða 1 = 84,84 &times; 10 prósent &divide; (1 – 10 prósent) 9,4267
- Skattaupphæð fyrir VSK-kóða 2 = 84,84 &times; 10 prósent &divide; (1 – 10 prósent) 9,4267

Skattupphæðin er námunduð eftir skattakóða:

- Sléttuð skattaupphæð fyrir VSK-kóða 1 = 9,43
- Sléttuð skattaupphæð fyrir VSK-kóða 2 = 9,43

Sléttaðri skattupphæð er úthlutað á hverja línu eftir VSK-kóða:

- Úthlutaðu skattfjárhæðinni fyrir söluskattskóða 1 (9,43) í línu 1 (4,72) og línu 2 (4,71).
- Úthlutaðu skattfjárhæðinni fyrir söluskattskóða 2 (9,43) í línu 1 (4,72) og línu 2 (4,71).

## <a name="example-5"></a>Dæmi 5

### <a name="parameter-values"></a>Gildi færibreytu

| Útreikningsaðferð | Sléttað eftir                | Uppruni                   | Jaðargrunnur       |
| ------------------ | -------------------------- | ------------------------ | ------------------- |
| Lína               | VSK-kóðasamsetning | Prósenta af nettóupphæð | Nettóupphæð á línu |

### <a name="calculation-and-rounding-behavior"></a>Útreiknings- og sléttunarhegðun

| Línunúmer | VSK-kóði | Uppruni upphæðar | Upphæð virðisaukaskatts |
| ----------- | -------------- | ------------- | ---------------- |
| 1           | Kóði 1         | 42,42         | 4,25             |
| 1           | Kóði 2         | 42,42         | 4,24             |
| 2           | Kóði 1         | 42,42         | 4,24             |
| 2           | Kóði 2         | 42,42         | 4,24             |

Grunnfjárhæð skatts er reiknuð fyrir hverja línu:

- **1. lína:** 42,42
- **Lína 2:** 42,42

Skattupphæðin er reiknuð út eftir skattakóða:

- **Lína 1:**

    - Skattaupphæð fyrir VSK-kóða 1 = 42,42 &times; 10 prósent = 4,242
    - skattaupphæð fyrir VSK-kóða 2 = 42,42 &times; 10 prósent = 4,242

- **Lína 2:**

    - Skattaupphæð fyrir VSK-kóða 1 = 42,42 &times; 10 prósent = 4,242
    - Skattaupphæð fyrir VSK-kóða 2 = 42,42 &times; 10 prósent = 4,242

Skattupphæðin er námunduð eftir skattakóðasamsetningu:

- Heildarfjárhæð söluskatts = 4,242 + 4,242 + 4,242 = 16,968, sem er námundað upp í 16,97

Sléttaðri skattupphæð er úthlutað á hverja línu eftir VSK-kóða:

- Úthluta skal söluskattsupphæð (16,97) í línu 1 og línu 2:

    - **Lína 1:**

        - Skattaupphæð fyrir VSK-kóða 1 = 4,25
        - Skattaupphæð fyrir VSK-kóða 2 = 4,24

    - **Lína 2:**

        - Skattaupphæð fyrir VSK-kóða 1 = 4,24
        - Skattaupphæð fyrir VSK-kóða 2 = 4,24

## <a name="example-6"></a>Dæmi 6

### <a name="parameter-values"></a>Gildi færibreytu

| Útreikningsaðferð | Sléttað eftir                | Uppruni                   | Jaðargrunnur                 |
| ------------------ | -------------------------- | ------------------------ | ----------------------------- |
| Lína/Samtals         | VSK-kóðasamsetning | Prósenta af nettóupphæð | Nettóupphæð af reikningsstöðu |

### <a name="calculation-and-rounding-behavior"></a>Útreiknings- og sléttunarhegðun

| Línunúmer | VSK-kóði | Uppruni upphæðar | Upphæð virðisaukaskatts |
| ----------- | -------------- | ------------- | ---------------- |
| 1           | Kóði 1         | 42,42         | 4,25             |
| 1           | Kóði 2         | 42,42         | 4,24             |
| 2           | Kóði 1         | 42,42         | 4,24             |
| 2           | Kóði 2         | 42,42         | 4,24             |

Grunnfjárhæð skatts er reiknuð fyrir hvert skjal:

- Grunnupphæð skatts = 42,42 + 42,42 = 84,84

Skattupphæðin er reiknuð út eftir skattakóða:

- Skattaupphæð fyrir VSK-kóða 1 = 84,84 &times; 10 prósent = 8,484
- Skattaupphæð fyrir VSK-kóða 2 = 84,84 &times; 10 prósent = 8,484

Skattupphæðin er námunduð eftir skattakóðasamsetningu:

- Heildarfjárhæð söluskatts = 8,484 + 8,484 = 16,968, sem er námundað upp í 16,97

Sléttaðri skattupphæð er úthlutað á hverja línu eftir VSK-kóða:

- Úthluta skal söluskattsupphæð (16,97) í línu 1 og línu 2:

    - **Lína 1:**

        - Skattaupphæð fyrir VSK-kóða 1 = 4,25
        - Skattaupphæð fyrir VSK-kóða 2 = 4,24

    - **Lína 2:**

        - Skattaupphæð fyrir VSK-kóða 1 = 4,24
        - Skattaupphæð fyrir VSK-kóða 2 = 4,24

## <a name="example-7"></a>Dæmi 7

### <a name="parameter-values"></a>Gildi færibreytu

| Útreikningsaðferð | Sléttað eftir                | Uppruni                              | Jaðargrunnur       |
| ------------------ | -------------------------- | ----------------------------------- | ------------------- |
| Lína               | VSK-kóðasamsetning | Reiknuð prósenta af nettóupphæð | Nettóupphæð á línu |

### <a name="calculation-and-rounding-behavior"></a>Útreiknings- og sléttunarhegðun

| Línunúmer | VSK-kóði | Uppruni upphæðar | Upphæð virðisaukaskatts |
| ----------- | -------------- | ------------- | ---------------- |
| 1           | Kóði 1         | 42,42         | 4,72             |
| 1           | Kóði 2         | 42,42         | 4,71             |
| 2           | Kóði 1         | 42,42         | 4,71             |
| 2           | Kóði 2         | 42,42         | 4,72             |

Grunnfjárhæð skatts er reiknuð fyrir hverja línu:

- **1. lína:** 42,42
- **Lína 2:** 42,42

Skattupphæðin er reiknuð út eftir skattakóða:

- **Lína 1:**

    - Skattaupphæð fyrir VSK-kóða 1 = 42,42 &times; 10 prósent &divide; (1 – 10 prósent) 4,7133
    - Skattaupphæð fyrir VSK-kóða 2 = 42,42 &times; 10 prósent &divide; (1 – 10 prósent) 4,7133

- **Lína 2:**

    - Skattaupphæð fyrir VSK-kóða 1 = 42,42 &times; 10 prósent &divide; (1 – 10 prósent) 4,7133
    - Skattaupphæð fyrir VSK-kóða 2 = 42,42 &times; 10 prósent &divide; (1 – 10 prósent) 4,7133

Skattupphæðin er námunduð eftir skattakóðasamsetningu:

- Heildarfjárhæð söluskatts = 4,7133 + 4,7133 + 4,7133 = 18,8532, sem er námundað upp í 18,86

Sléttaðri skattupphæð er úthlutað á hverja línu eftir VSK-kóða:

- Úthluta skal söluskattsupphæð (18,86) í línu 1 og línu 2:

    - **Lína 1:**

        - Skattaupphæð fyrir VSK-kóða 1 = 4,72
        - Skattaupphæð fyrir VSK-kóða 2 = 4,71

    - **Lína 2:**

        - Skattaupphæð fyrir VSK-kóða 1 = 4,71
        - Skattaupphæð fyrir VSK-kóða 2 = 4,72

## <a name="example-8"></a>Dæmi 8

### <a name="parameter-values"></a>Gildi færibreytu

| Útreikningsaðferð | Sléttað eftir                | Uppruni                              | Jaðargrunnur                 |
| ------------------ | -------------------------- | ----------------------------------- | ----------------------------- |
| Lína/Samtals         | VSK-kóðasamsetning | Reiknuð prósenta af nettóupphæð | Nettóupphæð af reikningsstöðu |

### <a name="calculation-and-rounding-behavior"></a>Útreiknings- og sléttunarhegðun

| Línunúmer | VSK-kóði | Uppruni upphæðar | Upphæð virðisaukaskatts |
| ----------- | -------------- | ------------- | ---------------- |
| 1           | Kóði 1         | 42,42         | 4,72             |
| 1           | Kóði 2         | 42,42         | 4,71             |
| 2           | Kóði 1         | 42,42         | 4,71             |
| 2           | Kóði 2         | 42,42         | 4,72             |

Grunnfjárhæð skatts er reiknuð fyrir hvert skjal:

- Grunnupphæð skatts = 42,42 + 42,42 = 84,84

Skattupphæðin er reiknuð út eftir skattakóða:

- Skattaupphæð fyrir VSK-kóða 1 = 84,84 &times; 10 prósent &divide; (1 – 10 prósent) 9,4267
- Skattaupphæð fyrir VSK-kóða 2 = 84,84 &times; 10 prósent &divide; (1 – 10 prósent) 9,4267

Skattupphæðin er námunduð eftir skattakóðasamsetningu:

- Heildarupphæð virðisaukaskatts = 9,4267 + 9,4267 = 18,86, sem er námundað að 18,86

Sléttaðri skattupphæð er úthlutað á hverja línu eftir VSK-kóða:

- Úthluta skal söluskattsupphæð (18,86) í línu 1 og línu 2:

    - **Lína 1:**

        - Skattaupphæð fyrir VSK-kóða 1 = 4,72
        - Skattaupphæð fyrir VSK-kóða 2 = 4,71

    - **Lína 2:**

        - Skattaupphæð fyrir VSK-kóða 1 = 4,71
        - Skattaupphæð fyrir VSK-kóða 2 = 4,72

## <a name="additional-resources"></a>Frekari upplýsingar

- [Útreikningsaðferðir VSK í upprunareitnum](sales-tax-calculation-methods-origin-field.md)
- [Virðisaukaskattur byggður á jaðargrunns- og útreikningsaðferðum](marginal-base-field.md)
- [Valkostir heildarupphæðar og tímabilsútreikninga fyrir VSK-kóða](whole-amount-interval-options-sales-tax-codes.md)
