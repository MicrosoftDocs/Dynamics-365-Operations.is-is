---
title: ADDDAYS ER aðgerð
description: Í þessari grein er að finna upplýsingar um hvernig ADDDAYS rafræn skýrslugerðarvirkni (ER) er notuð.
author: kfend
ms.date: 12/03/2019
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
ms.openlocfilehash: 69273794def0dc52dc8e31615c319ccf5067fa77
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9274140"
---
# <a name="adddays-er-function"></a>ADDDAYS ER aðgerð

[!include [banner](../includes/banner.md)]

Aðgerðin `ADDDAYS` reiknar út *DateTime*-gildi sem er tilgreindur fjöldi daga fyrir eða eftir tiltekinn upphafsdag.

## <a name="syntax"></a>Málskipun

```vb
ADDDAYS (datetime, days)
```

## <a name="arguments"></a>Frumbreytur

`datetime`: *DateTime*

Dagsetningar-/tímagildi sem táknar upphafsdag.

`days`: *Heiltala*

Dagafjöldi fyrir eða eftir `datetime`.

## <a name="return-values"></a>Skilagildi

*DateTime*

Dagsetningar-/tímagildið sem verður til.

## <a name="usage-notes"></a>Notkunarbréf

Jákvætt gildi fyrir `days` skilar framtíðardegi. Neikvætt gildi skilar liðinni dagsetningu.

## <a name="example-1"></a>Dæmi 1

`ADDDAYS (NOW(), 7)` skilar dagsetningu og tíma sjö daga fram í tímann.

## <a name="example-2"></a>Dæmi 2

`ADDDAYS (NOW(), -3)` skilar dagsetningu og tíma þrjá daga aftur í tímann.

## <a name="additional-resources"></a>Frekari upplýsingar

[Dagsetningar og tímavirkni](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
