---
title: FA_SUM ER-aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin FA_SUM í rafrænni skýrslugerð (ER) er notuð.
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
ms.openlocfilehash: 03bed091350b39601edb22b5af6bda5a83af47eb
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041355"
---
# <a name="FA_SUM">FA_SUM ER-aðgerð</a>

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
