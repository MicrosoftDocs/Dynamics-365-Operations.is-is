---
title: VALUE ER aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin VALUE í rafrænni skýrslugerð (ER) er notuð.
author: NickSelin
manager: kfend
ms.date: 12/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 160dd81baa43702b2deea1e3eea20080fca122ca
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917627"
---
# <a name="VALUE">VALUE ER aðgerð</a>

[!include [banner](../includes/banner.md)]

Aðgerðin `VALUE` skilar *Raun*-gildi sem er umreiknað úr tilgreindum streng.

## <a name="syntax"></a>Málskipun

```
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
