---
title: DAYS ER aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin DAYS í rafrænni skýrslugerð (ER) er notuð.
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
ms.openlocfilehash: 310359a29a506d69d1f34aaa710a82b0f2ea528e
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746892"
---
# <a name="days-er-function"></a>DAYS ER aðgerð

[!include [banner](../includes/banner.md)]

Aðgerðin `DAYS` skilar *heiltölu*-gildi sem sýnir fjölda daga milli einnar tilgreindrar dagsetningar og annarrar tilgreindrar dagsetningar.

## <a name="syntax"></a>Málskipun

```vb
DAYS (date 1, date 2) as Integer
```

## <a name="arguments"></a>Frumbreytur

`date 1`: *Dagsetning*

Dagsetningargildi sem táknar upphafsdagsetninguna fyrir útreikning á fjölda daga.

`date 2`: *Dagsetning*

Dagsetningargildi sem táknar lokadagsetninguna fyrir útreikning á fjölda daga.

## <a name="return-values"></a>Skilagildi

*Heiltala*

Tölugildið sem verður til.

## <a name="usage-notes"></a>Notkunarbréf

Aðgerðin `DAYS` skilar jákvæðu gildi þegar fyrsta dagsetningin er seinna en seinni dagsetningin, hún skilar **0** (núll) þegar fyrsta dagsetningin er jafngild annarri dagsetningu og hún skilar neikvæðu gildi þegar fyrsta dagsetningin er á undan seinni dagsetningunni.

## <a name="example"></a>Dæmi

`DAYS (TODAY (), DATEVALUE( DATETIMEFORMAT( ADDDAYS ( NOW(), 1), "yyyyMMdd"), "yyyyMMdd"))` skilar **-1**.

## <a name="additional-resources"></a>Frekari upplýsingar

[Dagsetningar og tímavirkni](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]