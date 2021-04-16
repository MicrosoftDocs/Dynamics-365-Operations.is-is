---
title: SESSIONTODAY ER aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin SESSIONTODAY í rafrænni skýrslugerð (ER) er notuð.
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
ms.openlocfilehash: 6d0fcbbf1a1fb0809e3f76161314f38bcd8a74aa
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746772"
---
# <a name="sessiontoday-er-function"></a>SESSIONTODAY ER aðgerð

[!include [banner](../includes/banner.md)]

Aðgerðin `SESSIONTODAY` skilar *Date*-gildi sem táknar setudagsetningu núverandi hugbúnaðar.

## <a name="syntax"></a>Málskipun

```vb
SESSIONTODAY ()
```

## <a name="return-values"></a>Skilagildi

*Dagsetning*

Dagsetningargildið sem verður til.

## <a name="example"></a>Dæmi

`DATEFORMAT (SESSIONTODAY (), "d", "DE")` skilar núverandi setudagsetningu hugbúnaðar, 24. desember 2015, sem strengnum  **"24-12-2015"**, byggt á valinni þýskri menningu og tilgreindu sniði.

## <a name="additional-resources"></a>Frekari upplýsingar

[Dagsetningar og tímavirkni](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]