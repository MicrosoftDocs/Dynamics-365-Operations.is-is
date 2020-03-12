---
title: ADDDAYS ER aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin ADDAYS í rafrænni skýrslugerð (ER) er notuð.
author: NickSelin
manager: kfend
ms.date: 12/03/2019
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
ms.openlocfilehash: 08b9727fb34210fecff31826cc1f2b8da022156b
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/12/2020
ms.locfileid: "3042459"
---
# <a name="ADDDAYS">ADDDAYS ER aðgerð</a>

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
