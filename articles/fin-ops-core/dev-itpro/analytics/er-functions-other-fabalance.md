---
title: FA_BALANCE ER-aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin FA_BALANCE í rafrænni skýrslugerð (ER) er notuð.
author: NickSelin
manager: kfend
ms.date: 12/17/2019
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
ms.openlocfilehash: 37c440a5c626016ebdb75703a2be63c9a1a2b560
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/09/2021
ms.locfileid: "5567593"
---
# <a name="fa_balance-er-function"></a>FA_BALANCE ER-aðgerð

[!include [banner](../includes/banner.md)]

Aðgerðin `FA_BALANCE` skilar *Ílát (skrá)*-gildi sem samanstendur af gögnum um varanleika fastafjármuna fyrir tiltekinn hlut í varanlegum rekstrarfjármunum, kóða fyrir virðislíkan, skýrsluár og skýrsludag.

## <a name="syntax"></a>Málskipun

```vb
FA_BALANCE (fixed asset code, value model code, reporting year, reporting date)
```

## <a name="arguments"></a>Frumbreytur

`fixed asset code`: *Strengur*

Gildið *Strengur* sem táknar kóða fastafjármagnsliða sem staðan er reiknuð fyrir.

`value model code`: *Strengur*

Gildið *Strengur* sem táknar kóða virðislíkans sem staðan er reiknuð fyrir.

`reporting year`: *Upptalningargildi*

Upptalningargildi forritsupptalningarinnar **AssetYear** sem skilgreinir tímabil fyrir útreikning á stöðu.

`reporting date`: *Dagsetning*

Gildið *Dagsetning* sem skilgreinir dagsetningu fyrir útreikning á stöðu.

## <a name="return-values"></a>Skilagildi

*Gámur (skrá)*

Skráargildið sem verður til.

## <a name="example"></a>Dæmi

`FA_ BALANCE ("COMP-000001", "Current", AxEnumAssetYear.ThisYear, SESSIONTODAY ())` skilar tilbúnum gagnageymi fyrir stöðu eignar **"COMP-000001"** sem hefur **"Núverandi"** gildislíkan á núverandi setudagsetningu forrits.

## <a name="additional-resources"></a>Frekari upplýsingar

[Other (lénsértæk virkni fyrir viðskipti)](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]