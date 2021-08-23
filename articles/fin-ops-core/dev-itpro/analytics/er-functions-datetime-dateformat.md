---
title: DATEFORMAT ER-aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin DATEFORMAT í rafrænni skýrslugerð (ER) er notuð.
author: NickSelin
ms.date: 01/04/2021
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
ms.openlocfilehash: 1e535f779e1fb87e6e14261df542f39e47323611a55483f03eba18ec379e92ba
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6770886"
---
# <a name="dateformat-er-function"></a>DATEFORMAT ER-aðgerð

[!include [banner](../includes/banner.md)]

Aðgerðin `DATEFORMAT` skilar *String*-gildi sem setur fram tiltekið dagsetningargildi sem texta á tilteknu sniði og í valinni tiltekinni [menningu](/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes). Fyrir upplýsingar um studd snið skal sjá [staðlað](/dotnet/standard/base-types/standard-date-and-time-format-strings) og [sérsniðna](/dotnet/standard/base-types/custom-date-and-time-format-strings).

## <a name="syntax-1"></a>Málskipun 1

```vb
DATEFORMAT (date, format)
```

## <a name="syntax-2"></a>Málskipun 2

```vb
DATEFORMAT (date, format, culture)
```

## <a name="arguments"></a>Frumbreytur

`date`: *Dagsetning*

Dagsetningargildi sem táknar dagsetningu til að forsníða.

`format`: *Strengur*

Snið úttaksstrengsins.

> [!NOTE]
> Sniðstrengurinn tekur tillit til há- og lágstafa þegar notað er annaðhvort staðlað snið eða sérstillt snið. Til dæmis skilar [staðlaða](/dotnet/standard/base-types/standard-date-and-time-format-strings) „d“-sniðsákvörðunin dagsetningunni með því að nota stutt dagsetningarsnið á meðan staðlaða „D“-sniðsákvörðunin skilar dagsetningunni með því að nota langt dagsetningarsnið. Auk þess skilar [sérstillt](/dotnet/standard/base-types/custom-date-and-time-format-strings) „M“-sniðsákvörðun mánuðinum frá 1 til 12 á meðan sérstillt „m“-sniðsákvörðun skilar mínútu frá 0 til 59.

`culture`: *Strengur*

Menningin sem á að nota til að forsníða.

## <a name="return-values"></a>Skilagildi

*Strengur*

Strenggildið sem myndast.

## <a name="usage-notes"></a>Notkunarbréf

Ef menningin er ekki skilgreind sem frumbreyta fyrir kallaða aðgerð er gildi `culture` skilgreint af samhengi köllunar. Til dæmis, ef aðgerðin `DATEFORMAT` er kölluð með því að nota málskipan 1 á rafrænni skýrslugerð (ER) sniði fyrir **FILE**-þáttinn sem er stillt til að nota þýska menningu verður umbreytingin gerð með því að nota þýska menninguna. Sjálfgefið gildi `culture` er **EN-US**.

## <a name="example-1"></a>Dæmi 1

`DATEFORMAT (TODAY (), "dd-MM-yyyy")` skilar núverandi dagsetningargildi hugbúnaðarþjóns, 24. desember, 2015, sem strenginn **"24-12-2015"**, miðað við tilgreint sérsniðið snið.

## <a name="example-2"></a>Dæmi 2

`DATEFORMAT (SESSIONTODAY (), "d", "DE")` skilar núverandi setudagsetningu hugbúnaðar, 24. desember 2015, sem strengnum  **"24-12-2015"**, byggt á valinni þýskri menningu og tilgreindu sniði.

## <a name="additional-resources"></a>Frekari upplýsingar

[Dagsetningar og tímavirkni](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]