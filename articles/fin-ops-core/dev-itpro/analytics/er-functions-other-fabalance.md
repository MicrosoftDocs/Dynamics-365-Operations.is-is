---
title: FA_BALANCE ER-aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin FA_BALANCE í rafrænni skýrslugerð (ER) er notuð.
author: NickSelin
manager: kfend
ms.date: 12/17/2019
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
ms.openlocfilehash: 0907cb8cb4bc1e90b9fb59eccedb699a894b5cc9
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916017"
---
# <a name="FA_BALANCE">FA_BALANCE ER-aðgerð</a>

[!include [banner](../includes/banner.md)]

Aðgerðin `FA_BALANCE` skilar *Ílát (skrá)*-gildi sem samanstendur af gögnum um varanleika fastafjármuna fyrir tiltekinn hlut í varanlegum rekstrarfjármunum, kóða fyrir virðislíkan, skýrsluár og skýrsludag.

## <a name="syntax"></a>Málskipun

```
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