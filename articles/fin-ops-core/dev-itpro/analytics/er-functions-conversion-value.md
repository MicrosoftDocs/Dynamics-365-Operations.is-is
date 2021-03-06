---
title: VALUE ER aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin VALUE í rafrænni skýrslugerð (ER) er notuð.
author: NickSelin
ms.date: 12/05/2019
ms.topic: article
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
ms.openlocfilehash: 2252823d98b63d36d9bb195696abef34ac9c98b6
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5752581"
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