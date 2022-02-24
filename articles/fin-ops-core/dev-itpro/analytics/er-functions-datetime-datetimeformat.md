---
title: DATETIMEFORMAT ER-aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin DATETIMEFORMAT í rafrænni skýrslugerð (ER) er notuð.
author: NickSelin
manager: kfend
ms.date: 01/04/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
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
ms.openlocfilehash: 90bd2900434b1be509f72ec82375e52ea32bc424
ms.sourcegitcommit: 7cfe8931dd454e811a691f5118a4ecae7ba4b478
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/04/2021
ms.locfileid: "4825374"
---
# <a name="datetimeformat-er-function"></a>DATETIMEFORMAT ER-aðgerð

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

> [!NOTE]
> Sniðstrengurinn tekur tillit til há- og lágstafa þegar notað er annaðhvort staðlað snið eða sérstillt snið. Til dæmis skilar [staðlaða](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) „d“-sniðsákvörðunin dagsetningunni með því að nota stutt dagsetningarsnið á meðan staðlaða „D“-sniðsákvörðunin skilar dagsetningunni með því að nota langt dagsetningarsnið. Auk þess skilar [sérstillt](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx) „M“-sniðsákvörðun mánuðinum frá 1 til 12 á meðan sérstillt „m“-sniðsákvörðun skilar mínútu frá 0 til 59.

`culture`: *Strengur*

Menningin sem á að nota til að forsníða.

## <a name="return-values"></a>Skilagildi

*Strengur*

Strenggildið sem myndast.

## <a name="usage-notes"></a>Notkunarbréf

Ef menningin er ekki skilgreind sem frumbreyta fyrir kallaða aðgerð er gildi `culture` skilgreint af samhengi köllunar. Til dæmis, ef aðgerðin `DATETIMEFORMAT` er kölluð með því að nota málskipan 1 á rafrænni skýrslugerð (ER) sniði fyrir **FILE**-þáttinn sem er stillt til að nota þýska menningu verður umbreytingin gerð með því að nota þýska menninguna. Sjálfgefið gildi `culture` er **EN-US**.

Þegar aðgerðin `DATETIMEFORMAT` breytir tilteknu gildi fyrir dagsetningu/tíma tekur það tillit til tímabeltisstillingar notanda hugbúnaðar sem er að keyra ER-sniðið sem aðgerðin er kölluð í samhengi við.

## <a name="example-1"></a>Dæmi 1

`DATETIMEFORMAT (NOW(), "dd-MM-yyyy")` skilar núverandi dagsetningar-/tímagildi hugbúnaðarþjóns, 24. desember, 2015, sem **"24-12-2015"**, miðað við tilgreint sérsniðið snið.

## <a name="example-2"></a>Dæmi 2

`DATETIMEFORMAT (SESSIONNOW(), "d", "DE")` skilar núverandi dagsetningar-/tímagildi setu hugbúnaðar, 24. desember 2015, sem **"24.12.2015"**, byggt á valinni þýskri menningu og tilgreindu sniði.

## <a name="example-3"></a>Dæmi 3

`DATETIMEFORMAT (DATETIMEVALUE( "2019-11-12T09:00:00.0000000-07:00", "O"), "O")` skilar strengjagildinu **2019-11-12T08:00:00.0000000-08:00** þegar kallað er á aðgerðina í ferli sem var sett af stað af notanda forrits sem er með tímabeltið **(GMT-08:00) Kyrrahafstími (Bandaríkin og Kanada)** í hlutanum **Kjörstillingar tungumáls og lands/svæðis**.

## <a name="additional-resources"></a>Frekari upplýsingar

[Dagsetningar og tímavirkni](er-functions-category-datetime.md)
