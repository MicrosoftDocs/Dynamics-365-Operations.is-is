---
title: CONVERTCURRENCY ER-aðgerð
description: Þessi grein veitir upplýsingar um hvernig aðgerðin CONVERTCURRENCY Rafræn skýrslugerð (ER) er notuð.
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
ms.openlocfilehash: e51086d977652e4be4c19390a824d4f4507b60d3
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8898463"
---
# <a name="convertcurrency-er-function"></a>CONVERTCURRENCY ER-aðgerð

[!include [banner](../includes/banner.md)]

Aðgerðin `CONVERTCURRENCY` skilar *raungildi* sem sýnir niðurstöður umreiknings á tilgreindri peningaupphæð frá tilgreindum upprunagjaldmiðli til tilgreinds markgjaldmiðils með því að nota stillingar tilgreinds fyrirtækis á tilteknum degi.

## <a name="syntax"></a>Málskipun

```vb
CONVERTCURRENCY (amount, source currency, target currency, date, company)
```

## <a name="arguments"></a>Frumbreytur

`amount`: *Heiltala* eða *Raun*

Tölugildi sem táknar peningaupphæðina sem þarf að breyta.

`source currency`: *Strengur*

Kóði upprunagjaldmiðils.

`target currency`: *Strengur*

Kóði markgjaldmiðils.

`date`: *Dagsetning*

Gildið *Dagsetning* sem táknar dagsetninguna sem er notuð til að ákvarða gengi viðskipta.

`company`: *Strengur*

Gildið *Strengur* sem táknar kóða fyrirtækisins sem veitir stillingarnar sem notaðar eru við umreikninginn.

## <a name="return-values"></a>Skilagildi

*Rauntala*

Tölugildið sem verður til.

## <a name="example"></a>Dæmi

`CONVERTCURRENCY (1, "EUR", "USD", TODAY(), "DEMF")` skilar jafngildi einni evru í Bandarískum dollurum á dagsetningu núverandi setu, byggða á stillingum **DEMF**-fyrirtækisins.

## <a name="additional-resources"></a>Frekari upplýsingar

[Other (lénsértæk virkni fyrir viðskipti)](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]