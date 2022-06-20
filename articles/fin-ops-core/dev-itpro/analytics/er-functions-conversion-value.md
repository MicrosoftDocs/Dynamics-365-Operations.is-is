---
title: VALUE ER aðgerð
description: Þessi grein veitir upplýsingar um hvernig aðgerðin VALUE rafræn skýrslugerð (ER) er notuð.
author: NickSelin
ms.date: 12/05/2019
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e96d274962ad79969a3158f7e352d3c72bd4072c
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8892981"
---
# <a name="value-er-function"></a>VALUE ER aðgerð

[!include [banner](../includes/banner.md)]

Aðgerðin `VALUE` skilar *Raun*-gildi sem er umreiknað úr tilgreindum streng.

## <a name="syntax"></a>Málskipun

```vb
VALUE (text)
```

## <a name="arguments"></a>Frumbreytur

`text`: *Strengur*

Strengjagildi sem þarf umreikna í tölulegt gildi.

## <a name="return-values"></a>Skilagildi

*Rauntala*

Tölugildið sem verður til.

## <a name="usage-notes"></a>Notkunarbréf

Kommur og punktar (.) skoðast sem skiltákn aukastafa, og bandstrik fremst (-) er notað sem neikvætt formerki. Undantekningu er beitt á keyrslutíma ef tilgreindur strengur inniheldur önnur tákn sem eru ekki tölur.

## <a name="example-1"></a>Dæmi 1

`VALUE ("1 234,56")` gerir undantekningu.

## <a name="example-2"></a>Dæmi 2

`VALUE ("1234,56")` skilar **1234,56**.

## <a name="additional-resources"></a>Frekari upplýsingar

[Aðgerðir fyrir umbreytingu á gerð](er-functions-category-type-conversion.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]