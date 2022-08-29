---
title: JSONVALUE ER-aðgerð
description: Þessi grein veitir upplýsingar um hvernig JSONVALUE rafræn skýrslugerð (ER) aðgerðin er notuð.
author: kfend
ms.date: 10/25/2021
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
ms.openlocfilehash: fba1141bce91fd7c9da3cd21aef13ce99329f379
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9267964"
---
# <a name="jsonvalue-er-function"></a>JSONVALUE ER-aðgerð

[!include [banner](../includes/banner.md)]

Aðgerðin `JSONVALUE` þáttar gögn í JavaScript Object Notation (JSON) sniði sem er aðgengilegt á tilgreindri slóð og dregur út tölugildi sem hefur tilgreint auðkenni. Hún skilar síðan útdregnu tölugildinu sem *Strengja*-gildi.

## <a name="syntax"></a>Málskipun

```vb
JSONVALUE (input, path)
```

## <a name="arguments"></a>Frumbreytur

`input`: *Strengur*

Gild slóð í gagnagjafa af gerðinni *Strengur* sem inniheldur JSON-gögn.

`path`: *Strengur*

Kennimerki tölugildis í JSON-gögnum. Notaðu skástrik (/) til að aðskilja nöfn tengdra JSON-hnúta. Notaðu hornklofa (\[\]) til að tilgreina stuðul tiltekins gildis í JSON-fylki. Athugaðu að tölusetning sem hefst á núlli er notuð fyrir þessa stuðla.

## <a name="return-values"></a>Skilagildi

*Strengur*

Textagildið sem verður til.

## <a name="example-1"></a>Dæmi 1

Gagnagjafinn **JsonField** inniheldur eftirfarandi gögn á JSON-sniði: **{"BuildNumber":"7.3.1234.1", "KeyThumbprint":"7366E"}**. Í þessu tilfelli skilar segðin `JSONVALUE (JsonField, "BuildNumber")` eftirfarandi gildi af gagnagerðinni *Strengur*: **"7.3.1234.1"**.

## <a name="example-2"></a>Dæmi 2

Gagnagjafinn **JsonField** af gerðinni *Reiknaður reitur* inniheldur eftirfarandi segð: `"{""workers"": [ {""name"": ""Adam"", ""age"": 30, ""emails"": [""AdamS@Contoso.com"", ""AdamS@Hotmail.com"" ]}, { ""name"": ""John"", ""age"": 21, ""emails"": [""JohnS@Contoso.com"", ""JohnS@Aol.com""]}]}"`

Þessi segð er skilgreind til að skila gildi [*Strengs*](er-formula-supported-data-types-primitive.md#string) sem táknar eftirfarandi gögn á JSON-sniði.

```json
{
    "workers": [
        {
            "name": "Adam",
            "age": 30,
            "emails": [ "AdamS@Contoso.com", "AdamS@Hotmail.com" ]
        },
        {
            "name": "John",
            "age": 21,
            "emails": [ "JohnS@Contoso.com", "JohnS@Aol.com" ]
        }
    ]
}
```

Í þessu tilviki skilar segðin `JSONVALUE(json, "workers/[1]/emails/[0]")` eftirfarandi gildi af gagnagerðinni *Strengur*: `JohnS@Contoso.com`.

## <a name="additional-resources"></a>Frekari upplýsingar

[Textaaðgerðir](er-functions-category-text.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
