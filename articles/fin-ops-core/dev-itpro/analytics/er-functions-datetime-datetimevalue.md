---
title: DATETIMEVALUE ER-aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin DATETIMEVALUE í rafrænni skýrslugerð (ER) er notuð.
author: NickSelin
ms.date: 12/03/2019
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
ms.openlocfilehash: db5b2c56f0c6dcc019419801821d7a6eae8a0e91
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/13/2021
ms.locfileid: "5891282"
---
# <a name="datetimevalue-er-function"></a>DATETIMEVALUE ER-aðgerð

[!include [banner](../includes/banner.md)]

Aðgerðin `DATETIMEVALUE` skilar *DateTime*-gildi sem er umreiknað úr gefnu textagildi á tilteknu sniði og í valinni tiltekinni [menningu](/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes) í dagsetningar-/tímagildi. Fyrir upplýsingar um studd snið skal sjá [staðlað](/dotnet/standard/base-types/standard-date-and-time-format-strings) og [sérsniðna](/dotnet/standard/base-types/custom-date-and-time-format-strings).

## <a name="syntax-1"></a>Málskipun 1

```vb
DATETIMEVALUE (text, format)
```

## <a name="syntax-2"></a>Málskipun 2

```vb
DATETIMEVALUE (text, format, culture)
```

## <a name="arguments"></a>Frumbreytur

`text`: *Strengur*

Texti sem táknar gildið til að forsníða.

`format`: *Strengur*

Snið gefins texta.

`culture`: *Strengur*

Menningin sem er notuð til að forsníða gefinn texta.

## <a name="return-values"></a>Skilagildi

*DateTime*

Dagsetningar-/tímagildið sem verður til.

## <a name="usage-notes"></a>Notkunarbréf

Þegar menningin er ekki skilgreind sem frumbreyta kallaðrar aðgerðar er gildið `culture` skilgreint af köllunarsamhenginu. Til dæmis, ef aðgerðin `DATETIMEVALUE` er kölluð með því að nota málskipan 1 á rafrænni skýrslugerð (ER) sniði fyrir **FILE**-þáttinn sem er stillt til að nota þýska menningu verður umbreytingin gerð með því að nota þýska menninguna. Sjálfgefið gildi `culture` er **EN-US**.

## <a name="example-1"></a>Dæmi 1

`DATETIMEVALUE ("21-Dec-2016 02:55:00", "dd-MMM-yyyy hh:mm:ss")` skilar **02:55 þann 21. desember, 2016**, byggt á tilteknu sérsniðnu sniði og sjálfgefninni menningu **EN-BNA** fyrir hugbúnaðinn.

## <a name="example-2"></a>Dæmi 2

`DATETIMEVALUE ("21-Gen-2016 02:55:00", "dd-MMM-yyyy hh:mm:ss", "IT")` skilar **02:55 þann 21. desember, 2016**, byggt á tilgreindu sérsniðnu sniði og menningu.

Hins vegar beitir `DATETIMEVALUE ("21-Gen-2016 02:55:00", "dd-MMM-yyyy hh:mm:ss", "EN-US")` undantekningu til að upplýsa notandann um að tilgreindur strengur sé ekki viðurkenndur sem gild dagsetning.

## <a name="additional-resources"></a>Frekari upplýsingar

[Dagsetningar og tímavirkni](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]