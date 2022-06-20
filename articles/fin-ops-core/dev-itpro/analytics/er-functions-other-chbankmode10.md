---
title: CH_BANK_MOD_10 ER-aðgerð
description: Þessi grein veitir upplýsingar um hvernig CH_BANK_MOD_10 rafræn skýrslugerð (ER) aðgerðin er notuð.
author: NickSelin
ms.date: 12/17/2019
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
ms.openlocfilehash: 494aa335ef170db0cd2f61a1d33391de474cd4bd
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8885028"
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


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]