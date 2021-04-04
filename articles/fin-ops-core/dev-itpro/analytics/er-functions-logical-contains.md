---
title: CONTAINS-aðgerð rafrænnar skýrslugerðar
description: Þetta efnisatriði inniheldur upplýsingar um hvernig CONTAINS-aðgerð rafrænnar skýrslugerðar er notuð.
author: NickSelin
manager: kfend
ms.date: 02/11/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
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
ms.openlocfilehash: 81964681688cebf870bc9b6c59aff0b7fdd82449
ms.sourcegitcommit: 08ac570bece3e4ee4a0f632f51623e328536dfcf
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/08/2021
ms.locfileid: "5557527"
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

Þessa aðgerð er hægt að nota til að tilgreina segð skilyrðis fyrir aðgerðina [FILTER](er-functions-list-filter.md) aðeins þegar tilheyrandi vörpun er skilgreind í [Regulatory Configuration Services](../../../finance/localizations/rcs-globalization-feature.md) til að fá aðgang að [Microsoft Dataverse](../data-entities/data-integration-cds.md). Annars er undantekning notuð á hönnunartíma. Skilaboðin sem birtast ráðleggja að nota aðgerðina [WHERE](er-functions-list-where.md) í staðinn fyrir aðgerðina `FILTER`.

## <a name="example-1"></a>Dæmi 1

Segðin `CONTAINS ("abc", "d")` skilar **FALSE** á meðan segðin `CONTAINS ("abc", "C")` skilar **TRUE**.

## <a name="example-2"></a>Dæmi 2

Segðin `CONTAINS (model.InvoiceBase.Customer.PostalAddress.Address, "DEU")` skilar **TRUE** ef gildið reitsins **Aðsetur** af gagngjafanum **líkan** innheldur strenginn **DEU**. Annars skilar hún **FALSE**.

## <a name="additional-resources"></a>Frekari upplýsingar

[Rökfræðiaðgerðir](er-functions-category-logical.md)
