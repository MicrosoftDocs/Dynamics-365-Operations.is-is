---
title: DATEVALUE ER-aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin DATEVALUE í rafrænni skýrslugerð (ER) er notuð.
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
ms.openlocfilehash: d760c3f874bfebad11b9497b136cb67df4e9ea61
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746940"
---
# <a name="datevalue-er-function"></a>DATEVALUE ER-aðgerð

[!include [banner](../includes/banner.md)]

Aðgerðin `DATEVALUE` skilar *Date*-gildi sem er umreiknað úr gefnu textagildi á tilteknu sniði og í valinni tiltekinni [menningu](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes) í dagsetningargildi. Fyrir upplýsingar um studd snið skal sjá [staðlað](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) og [sérsniðna](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx).

## <a name="syntax-1"></a>Málskipun 1

```vb
DATEVALUE (text, format)
```

## <a name="syntax-2"></a>Málskipun 2

```vb
DATEVALUE (text, format, culture)
```

## <a name="arguments"></a>Frumbreytur

`text`: *Strengur*

Texti sem táknar gildið til að forsníða.

`format`: *Strengur*

Snið gefins texta.

`culture`: *Strengur*

Menningin sem er notuð til að forsníða gefinn texta.

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