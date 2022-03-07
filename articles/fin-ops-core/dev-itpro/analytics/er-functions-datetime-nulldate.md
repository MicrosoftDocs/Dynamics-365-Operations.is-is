---
title: NULLDATE ER-aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin NULLDATE í rafrænni skýrslugerð (ER) er notuð.
author: NickSelin
ms.date: 12/04/2019
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
ms.openlocfilehash: 6ac8da3f18c7793512685d52dd64a9bd55bfb8fc
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746844"
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


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]