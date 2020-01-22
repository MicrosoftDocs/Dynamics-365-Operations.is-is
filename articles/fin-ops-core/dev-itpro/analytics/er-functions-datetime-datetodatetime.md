---
title: DATETODATETIME ER-aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin DATETODATETIME í rafrænni skýrslugerð (ER) er notuð.
author: NickSelin
manager: kfend
ms.date: 12/04/2019
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
ms.openlocfilehash: f9ce977b36cd96a27a228dba1bc8c8445bafd879
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916385"
---
# <a name="DATETODATETIME">DATETODATETIME ER-aðgerð</a>

[!include [banner](../includes/banner.md)]

Aðgerðin `DATETODATETIME` skilar *DateTime*-gildi sem er umreiknað úr gefnu dagsetningargildi í dagsetningar-/tímagildi í samræmdan alþjóðlegan tíma (meðaltími Greenwich \[GMT\]).

## <a name="syntax"></a>Málskipun

```
DATETODATETIME (date)
```

## <a name="arguments"></a>Frumbreytur

`date`: *Dagsetning*

Dagsetningargildi sem táknar dagsetningu til að umreikna.

## <a name="return-values"></a>Skilagildi

*DateTime*

Dagsetningar-/tímagildið sem verður til.

## <a name="example-1"></a>Dæmi 1

`DATETODATETIME (CompInfo. 'getCurrentDate()')` skilar dagsetningu gildandi Microsoft Dynamics 365 Finance-setu, 24. desember, 2015, sem **12/24 / 2015 12:00:00 AM**. Í þessu dæmi er **CompInfo** gagnagjafi rafrænnar skýrslugerðar (ER) fyrir **Finance and Operations/tafla** gerð og vísar til CompanyInfo töflunnar.

## <a name="example-2"></a>Dæmi 2

`DATETODATETIME (DATEVALUE ("2019-11-12T16:00:00.0000000-07:00", "O"))` skilar dagsetningar-/tímagildinu **11/12 / 2019 12:00:00 AM**.

## <a name="additional-resources"></a>Frekari upplýsingar

[Dagsetningar og tímavirkni](er-functions-category-datetime.md)
