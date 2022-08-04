---
title: DATETODATETIME ER-aðgerð
description: Þessi grein veitir upplýsingar um hvernig DATETODATETIME rafræn skýrslugerð (ER) aðgerðin er notuð.
author: NickSelin
ms.date: 12/04/2019
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
ms.openlocfilehash: 519932854dfd3e872433b0fb304e683c57cea1cb
ms.sourcegitcommit: 3289478a05040910f356baf1995ce0523d347368
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 07/01/2022
ms.locfileid: "9108498"
---
# <a name="datetodatetime-er-function"></a>DATETODATETIME ER-aðgerð

[!include [banner](../includes/banner.md)]

Aðgerðin `DATETODATETIME` skilar *DateTime*-gildi sem er umreiknað úr gefnu dagsetningargildi í dagsetningar-/tímagildi í samræmdan alþjóðlegan tíma (meðaltími Greenwich \[GMT\]).

## <a name="syntax"></a>Málskipun

```vb
DATETODATETIME (date)
```

## <a name="arguments"></a>Frumbreytur

`date`: *Dagsetning*

Dagsetningargildi sem táknar dagsetningu til að umreikna.

## <a name="return-values"></a>Skilagildi

*DateTime*

Dagsetningar-/tímagildið sem verður til.

## <a name="example-1"></a>Dæmi 1

`DATETODATETIME (CompInfo. 'getCurrentDate()')` skilar dagsetningu núverandi Microsoft Dynamics 365 Fjármálaþing, 24. desember 2015, sem **24/12/2015 12:00:00**. Í þessu dæmi, **CompInfo** er rafræn skýrslugerð (ER) gagnagjafi **fjármál og rekstur/Tafla** gerð, og það vísar í CompanyInfo töfluna.

## <a name="example-2"></a>Dæmi 2

`DATETODATETIME (DATEVALUE ("2019-11-12T16:00:00.0000000-07:00", "O"))` skilar dagsetningar-/tímagildinu **11/12 / 2019 12:00:00 AM**.

## <a name="additional-resources"></a>Frekari upplýsingar

[Dagsetningar og tímavirkni](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
