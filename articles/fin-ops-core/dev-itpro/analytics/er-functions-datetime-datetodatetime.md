---
title: DATETODATETIME ER-aðgerð
description: Þessi grein veitir upplýsingar um hvernig DATETODATETIME rafræn skýrslugerð (ER) aðgerðin er notuð.
author: kfend
ms.date: 12/04/2019
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
ms.openlocfilehash: 30fe75c7fd68edfff3e3778192723792d0f342ab
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9287309"
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
