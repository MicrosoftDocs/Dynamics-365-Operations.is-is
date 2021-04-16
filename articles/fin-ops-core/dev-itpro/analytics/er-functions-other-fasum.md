---
title: FA_SUM ER-aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin FA_SUM í rafrænni skýrslugerð (ER) er notuð.
author: NickSelin
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
ms.openlocfilehash: d6f380e384e591e7417cfa40c73f9be6575fb0f6
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5744296"
---
# <a name="fa_sum-er-function"></a>FA_SUM ER-aðgerð

[!include [banner](../includes/banner.md)]

Aðgerðin `FA_SUM` skilar *Ílát (skrá)*-gildi sem samanstendur af gögnum um upphæðir fastafjármuna fyrir tiltekinn hlut í varanlegum rekstrarfjármunum, kóða fyrir virðislíkan og dagsetningatímabil.

## <a name="syntax"></a>Málskipun

```vb
FA_SUM (fixed asset code, value model code, start date, end date)
```

## <a name="arguments"></a>Frumbreytur

`fixed asset code`: *Strengur*

Gildið *Strengur* sem táknar kóða fastafjármagnsliða sem staðan er reiknuð fyrir.

`value model code`: *Strengur*

Gildið *Strengur* sem táknar kóða virðislíkans sem staðan er reiknuð fyrir.

`start date`: *Dagsetning*

Gildið *Dagsetning* sem táknar upphafsdag tímabils sem fastafjárhæðir eru reiknaðar út fyrir.

`end date`: *Dagsetning*

Gildið *Dagsetning* sem táknar lokadag tímabils sem fastafjárhæðir eru reiknaðar út fyrir.

## <a name="return-values"></a>Skilagildi

*Gámur (skrá)*

Skráargildið sem verður til.

## <a name="example"></a>Dæmi

`FA_SUM ("COMP-000001", "Current", Date1, Date2)` skilar gagnaíláti fyrir fastaeignina **COMP-000001** sem hefur verið undirbúin fyrir virðislíkanið **Gildandi** og fyrir tímabil frá **Dagsetning1** til **Dagsetning2**.

## <a name="additional-resources"></a>Frekari upplýsingar

[Other (lénsértæk virkni fyrir viðskipti)](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]