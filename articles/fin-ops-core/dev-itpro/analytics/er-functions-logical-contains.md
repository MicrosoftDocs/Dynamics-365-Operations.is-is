---
title: CONTAINS-aðgerð rafrænnar skýrslugerðar
description: Þetta efnisatriði inniheldur upplýsingar um hvernig CONTAINS-aðgerð rafrænnar skýrslugerðar er notuð.
author: NickSelin
ms.date: 02/11/2021
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2021-02-01
ms.dyn365.ops.version: AX 10.0.18
ms.openlocfilehash: ae6c96b5754946ee971a8f47d4c618751d25f7e86fb9fb115861e97c5e6f536e
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6765147"
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
