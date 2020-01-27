---
title: SESSIONTODAY ER aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin SESSIONTODAY í rafrænni skýrslugerð (ER) er notuð.
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
ms.openlocfilehash: bcfb36d6e3fb8475546f7cfb420c4aca848ac896
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917466"
---
# <a name="SESSIONTODAY">SESSIONTODAY ER aðgerð</a>

[!include [banner](../includes/banner.md)]

Aðgerðin `SESSIONTODAY` skilar *Date*-gildi sem táknar setudagsetningu núverandi hugbúnaðar.

## <a name="syntax"></a>Málskipun

```
SESSIONTODAY ()
```

## <a name="return-values"></a>Skilagildi

*Dagsetning*

Dagsetningargildið sem verður til.

## <a name="example"></a>Dæmi

`DATEFORMAT (SESSIONTODAY (), "d", "DE")` skilar núverandi setudagsetningu hugbúnaðar, 24. desember 2015, sem strengnum  **"24-12-2015"**, byggt á valinni þýskri menningu og tilgreindu sniði.

## <a name="additional-resources"></a>Frekari upplýsingar

[Dagsetningar og tímavirkni](er-functions-category-datetime.md)
