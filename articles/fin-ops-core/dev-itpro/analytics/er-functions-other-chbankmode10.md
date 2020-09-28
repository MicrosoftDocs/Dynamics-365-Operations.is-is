---
title: CH_BANK_MOD_10 ER-aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin CH_BANK_MOD_10 í rafrænni skýrslugerð (ER) er notuð.
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
ms.openlocfilehash: c18a7f96096fbc6bbc7b6d15135c11bd70960d26
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744471"
---
# <a name="ch_bank_mod_10-er-function"></a>CH_BANK_MOD_10 ER-aðgerð

[!include [banner](../includes/banner.md)]

Aðgerðin `CH_BANK_MOD_10` skilar *Streng*-gildi sem táknar tilvísun kröfuhafa sem MOD10 segð, byggða á tölustöfum tilgreinds reikningsnúmers.

## <a name="syntax"></a>Málskipun

```vb
CH_BANK_MOD_10 (invoice number digits)
```

## <a name="arguments"></a>Frumbreytur

`invoice number digits`: *Strengur*

Textagildi sem stendur fyrir tölustafi reikningsnúmers.

## <a name="return-values"></a>Skilagildi

*Strengur*

Textagildið sem verður til.

## <a name="example"></a>Dæmi

`CH_BANK_MOD_10 ("VEND-200002")` skilar **3**.

## <a name="additional-resources"></a>Frekari upplýsingar

[Other (lénsértæk virkni fyrir viðskipti)](er-functions-category-other.md)
