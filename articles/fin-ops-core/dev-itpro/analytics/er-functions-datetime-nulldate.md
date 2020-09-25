---
title: NULLDATE ER-aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin NULLDATE í rafrænni skýrslugerð (ER) er notuð.
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
ms.openlocfilehash: edf43cc19636f51387504a7d9da73d757d96e558
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744288"
---
# <a name="nulldate-er-function"></a>NULLDATE ER-aðgerð

[!include [banner](../includes/banner.md)]

Aðgerðin `NULLDATE` skilar *Dagsetningar*-gildi sem táknar **núll** dagsetningu (1. janúar, 1900).

## <a name="syntax"></a>Málskipun

```vb
NULLDATE () as 
```

## <a name="return-values"></a>Skilagildi

*Dagsetning*

Dagsetningargildið sem verður til.

## <a name="example-1"></a>Dæmi 1

`DATEFORMAT (NULLDATE(), "yyyy-MM-dd")` skilar **núll** dagsetningu, 1. janúar, 1900, sem **"1900-01-01"**, byggt á tilgreindu sérsniðnu sniði.

## <a name="example-2"></a>Dæmi 2

Segðin `IF( Invoice.DocumentDate = NULLDATE(), true, false)` skilar **True** þegar gildið í reitnum **DocumentDate** er jafnt og **núll** dagsetning. Í þessu dæmi er **Invoice** gagnagjafi rafrænnar skýrslugerðar (ER) fyrir gerðina **Fjármála-/töfluskrá** og vísar til CustInvoiceJour-töflunnar.

## <a name="additional-resources"></a>Frekari upplýsingar

[Dagsetningar og tímavirkni](er-functions-category-datetime.md)
