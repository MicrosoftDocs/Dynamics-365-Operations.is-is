---
title: DATETIMEFORMAT ER-aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin DATETIMEFORMAT í rafrænni skýrslugerð (ER) er notuð.
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
ms.openlocfilehash: 9e550b0c7634c7aac3f8c597a1c1eac3f8125e3b
ms.sourcegitcommit: 3dede95a3b17de920bb0adcb33029f990682752b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/18/2020
ms.locfileid: "3070714"
---
# <a name="DATETIMEFORMAT">DATETIMEFORMAT ER-aðgerð</a>

[!include [banner](../includes/banner.md)]

Aðgerðin `DATETIMEFORMAT` skilar *String*-gildi sem setur fram tiltekið dagsetningar-/tímagildi sem texta á tilteknu sniði og í valinni tiltekinni [menningu](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes). Fyrir upplýsingar um studd snið skal sjá [staðlað](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) og [sérsniðna](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx).

## <a name="syntax-1"></a>Málskipun 1

```vb
DATETIMEFORMAT (datetime, format)
```

## <a name="syntax-2"></a>Málskipun 2

```vb
DATETIMEFORMAT (datetime, format, culture)
```

## <a name="arguments"></a>Frumbreytur

`datetime`: *DateTime*

Dagsetningar-/tímagildi sem táknar dagsetningu og tíma til að forsníða.

`format`: *Strengur*

Snið úttaksstrengsins.

`culture`: *Strengur*

Menningin sem á að nota til að forsníða.

## <a name="return-values"></a>Skilagildi

*Strengur*

Strenggildið sem myndast.

## <a name="usage-notes"></a>Notkunarbréf

Þegar menningin er ekki skilgreind sem frumbreyta kallaðrar aðgerðar er gildið `culture` skilgreint af köllunarsamhenginu. Til dæmis, ef aðgerðin `DATETIMEFORMAT` er kölluð með því að nota málskipan 1 á rafrænni skýrslugerð (ER) sniði fyrir **FILE**-þáttinn sem er stillt til að nota þýska menningu verður umbreytingin gerð með því að nota þýska menninguna. Sjálfgefið gildi `culture` er **EN-US**.

Þegar aðgerðin `DATETIMEFORMAT` breytir tilteknu gildi fyrir dagsetningu/tíma tekur það tillit til tímabeltisstillingar notanda hugbúnaðar sem er að keyra ER-sniðið sem aðgerðin er kölluð í samhengi við.

## <a name="example-1"></a>Dæmi 1

`DATETIMEFORMAT (NOW(), "dd-MM-yyyy")` skilar núverandi dagsetningar-/tímagildi hugbúnaðarþjóns, 24. desember, 2015, sem **"24-12-2015"**, miðað við tilgreint sérsniðið snið.

## <a name="example-2"></a>Dæmi 2

`DATETIMEFORMAT (SESSIONNOW(), "d", "DE")` skilar núverandi dagsetningar-/tímagildi setu hugbúnaðar, 24. desember 2015, sem **"24.12.2015"**, byggt á valinni þýskri menningu og tilgreindu sniði.

## <a name="example-3"></a>Dæmi 3

`DATETIMEFORMAT (DATETIMEVALUE( "2019-11-12T09:00:00.0000000-07:00", "O"), "O")` skilar strenggildinu **2019-11-12T08:00:00.0000000-08:00** þegar það er kallað í ferli sem var hafið af notanda forrits sem hefur tímabeltisgildið **(GMT-08: 00) Kyrrahafstími (BNA og Kanada)** í hlutanum **Val á tungumáli og landi/svæði**.

## <a name="additional-resources"></a>Frekari upplýsingar

[Dagsetningar og tímavirkni](er-functions-category-datetime.md)
