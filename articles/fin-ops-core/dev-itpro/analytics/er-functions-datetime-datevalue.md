---
title: DATEVALUE ER-aðgerð
description: Í þessari grein er að finna upplýsingar um hvernig DATEVALUE rafræn skýrslugerðarvirkni (ER) er notuð.
author: kfend
ms.date: 09/08/2021
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
ms.openlocfilehash: 290a4665d3527c0f0954c46cb0a0a14677b93218
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9268699"
---
# <a name="datevalue-er-function"></a>DATEVALUE ER-aðgerð

[!include [banner](../includes/banner.md)]

Þessi `DATEVALUE`-aðgerð skilar *[Date](er-formula-supported-data-types-primitive.md#date)*-gildi sem er umreiknað úr gefnu strengja-gildi á tilteknu sniði og í valinni tiltekinni [menningu](/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes) í dagsetningargildi. Fyrir upplýsingar um studd snið skal sjá [staðlað](/dotnet/standard/base-types/standard-date-and-time-format-strings) og [sérsniðna](/dotnet/standard/base-types/custom-date-and-time-format-strings).

## <a name="syntax-1"></a>Málskipun 1

```vb
DATEVALUE (text, format)
```

## <a name="syntax-2"></a>Málskipun 2

```vb
DATEVALUE (text, format, culture)
```

## <a name="arguments"></a>Frumbreytur

`text`: *[Strengur](er-formula-supported-data-types-primitive.md#string)*

Texti sem táknar gildið til að forsníða.

`format`: *Strengur*

Snið gefins texta. Fyrir upplýsingar um studd snið skal sjá [staðlað](/dotnet/standard/base-types/standard-date-and-time-format-strings) og [sérsniðna](/dotnet/standard/base-types/custom-date-and-time-format-strings).

`culture`: *Strengur*

Menningin sem er notuð til að forsníða gefinn texta. Fyrir upplýsingar um studdar menningar skal skoða [menningu](/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes).

## <a name="return-values"></a>Skilagildi

*Dagsetning*

Dagsetningargildið sem verður til.

## <a name="usage-notes"></a>Notkunarbréf

Þegar menningin er ekki skilgreind sem frumbreyta kallaðrar aðgerðar er gildið `culture` skilgreint af köllunarsamhenginu. Til dæmis, ef aðgerðin `DATEVALUE` er kölluð með því að nota málskipan 1 á rafrænni skýrslugerð (ER) sniði fyrir **FILE**-þáttinn sem er stillt til að nota þýska menningu verður umbreytingin gerð með því að nota þýska menninguna. Sjálfgefið gildi `culture` er **EN-US**.

## <a name="example-1"></a>Dæmi 1

`DATEVALUE ("21-Dec-2016", "dd-MMM-yyyy")` skilar dagsetnigargildinu **21. desember, 2016**, byggt á tilteknu sérsniðnu sniði og sjálfgefninni menningu **EN-BNA** fyrir hugbúnaðinn.

## <a name="example-2"></a>Dæmi 2

`DATEVALUE ("21-Gen-2016", "dd-MMM-yyyy", "IT")` skilar dagsetningargildinu **21. janúar, 2016**, byggt á tilgreindu sérsniðnu sniði og menningu.

Hins vegar beitir `DATEVALUE ("21-Gen-2016", "dd-MMM-yyyy", "EN-US")` undantekningu til að upplýsa notandann um að tilgreindur strengur sé ekki viðurkenndur sem gild dagsetning fyrir tilgreinda menningu.

## <a name="additional-resources"></a>Frekari upplýsingar

[Dagsetningar og tímavirkni](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
