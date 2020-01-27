---
title: DATEFORMAT ER-aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin DATEFORMAT í rafrænni skýrslugerð (ER) er notuð.
author: NickSelin
manager: kfend
ms.date: 12/03/2019
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
ms.openlocfilehash: c1453be0c93764f9f0364206822a9e3899061a58
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917581"
---
# <a name="DATEFORMAT">DATEFORMAT ER-aðgerð</a>

[!include [banner](../includes/banner.md)]

Aðgerðin `DATEFORMAT` skilar *String*-gildi sem setur fram tiltekið dagsetningargildi sem texta á tilteknu sniði og í valinni tiltekinni [menningu](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes). Fyrir upplýsingar um studd snið skal sjá [staðlað](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) og [sérsniðna](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx).

## <a name="syntax-1"></a>Málskipun 1

```
DATEFORMAT (date, format)
```

## <a name="syntax-2"></a>Málskipun 2

```
DATEFORMAT (date, format, culture)
```

## <a name="arguments"></a>Frumbreytur

`date`: *Dagsetning*

Dagsetningargildi sem táknar dagsetningu til að forsníða.

`format`: *Strengur*

Snið úttaksstrengsins.

`culture`: *Strengur*

Menningin sem á að nota til að forsníða.

## <a name="return-values"></a>Skilagildi

*Strengur*

Strenggildið sem myndast.

## <a name="usage-notes"></a>Notkunarbréf

Þegar menningin er ekki skilgreind sem frumbreyta kallaðrar aðgerðar er gildið `culture` skilgreint af köllunarsamhenginu. Til dæmis, ef aðgerðin `DATEFORMAT` er kölluð með því að nota málskipan 1 á rafrænni skýrslugerð (ER) sniði fyrir **FILE**-þáttinn sem er stillt til að nota þýska menningu verður umbreytingin gerð með því að nota þýska menninguna. Sjálfgefið gildi `culture` er **EN-US**.

## <a name="example-1"></a>Dæmi 1

`DATEFORMAT (TODAY (), "dd-MM-yyyy")` skilar núverandi dagsetningargildi hugbúnaðarþjóns, 24. desember, 2015, sem strenginn **"24-12-2015"**, miðað við tilgreint sérsniðið snið.

## <a name="example-2"></a>Dæmi 2

`DATEFORMAT (SESSIONTODAY (), "d", "DE")` skilar núverandi setudagsetningu hugbúnaðar, 24. desember 2015, sem strengnum  **"24-12-2015"**, byggt á valinni þýskri menningu og tilgreindu sniði.

## <a name="additional-resources"></a>Frekari upplýsingar

[Dagsetningar og tímavirkni](er-functions-category-datetime.md)
