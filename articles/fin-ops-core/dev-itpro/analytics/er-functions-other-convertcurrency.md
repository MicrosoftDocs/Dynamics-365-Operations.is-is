---
title: CONVERTCURRENCY ER-aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin CONVERTCURRENCY í rafrænni skýrslugerð (ER) er notuð.
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
ms.openlocfilehash: 1d0c168e07252f7c423271bc808f3fca3834077f
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041516"
---
# <a name="CONVERTCURRENCY">CONVERTCURRENCY ER-aðgerð</a>

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
