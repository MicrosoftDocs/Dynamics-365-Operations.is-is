---
title: CONTAINS-aðgerð rafrænnar skýrslugerðar
description: Þessi grein veitir upplýsingar um hvernig aðgerðin CONTAINS rafræn skýrslugerð (ER) er notuð.
author: kfend
ms.date: 02/11/2021
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2021-02-01
ms.dyn365.ops.version: AX 10.0.18
ms.custom: ''
ms.assetid: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
ms.openlocfilehash: 0b2831f8aec4847279953ebcea583c9218d214a7
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9273129"
---
# <a name="contains-er-function"></a>CONTAINS-aðgerð rafrænnar skýrslugerðar

[!include [banner](../includes/banner.md)]

Aðgerðin `CONTAINS` ákvarðar hvort tilgreindur innsláttur inniheldur tiltekinn texta. Hún skilar *Boole-gildinu* **TRUE** ef tilgreindur innsláttur inniheldur tilgreindan texta. Að öðrum kosti skilar hún *Boolean* gildinu **FALSE**.

## <a name="syntax"></a>Málskipun

```vb
CONTAINS (input, search text)
```

## <a name="arguments"></a>Frumbreytur

`input`: *Strengur*

Gild slóð atriðis fyrir gagnagjafa af gerðinni *Strengur* eða strengjafasti, gildi sem gæti innihaldið seinni frumbreytuna.

`search text`: *Strengur*

Gild slóð gagnagjafa af gerðinni *Strengur* eða strengjafasti, gildi sem fyrsta frumbreytan gæti innihaldið.

## <a name="return-values"></a>Skilagildi

*Boole*

*Boole*-gildið sem myndast.

## <a name="usage-notes"></a>Notkunarbréf

Þessa aðgerð er hægt að nota til að tilgreina segð skilyrðis fyrir aðgerðina [FILTER](er-functions-list-filter.md) aðeins þegar tilheyrandi vörpun er skilgreind í [Regulatory Configuration Services](../../../finance/localizations/rcs-globalization-feature.md) til að fá aðgang að [Microsoft Dataverse](/power-platform/admin/data-integrator). Annars er undantekning notuð á hönnunartíma. Skilaboðin sem birtast ráðleggja að nota aðgerðina [WHERE](er-functions-list-where.md) í staðinn fyrir aðgerðina `FILTER`.

## <a name="example-1"></a>Dæmi 1

Segðin `CONTAINS ("abc", "d")` skilar **FALSE** á meðan segðin `CONTAINS ("abc", "C")` skilar **TRUE**.

## <a name="example-2"></a>Dæmi 2

Segðin `CONTAINS (model.InvoiceBase.Customer.PostalAddress.Address, "DEU")` skilar **TRUE** ef gildið reitsins **Aðsetur** af gagngjafanum **líkan** innheldur strenginn **DEU**. Annars skilar hún **FALSE**.

## <a name="additional-resources"></a>Frekari upplýsingar

[Rökfræðiaðgerðir](er-functions-category-logical.md)
