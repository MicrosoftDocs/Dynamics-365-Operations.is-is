---
title: IF ER-aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin IF í rafrænni skýrslugerð (ER) er notuð.
author: NickSelin
manager: kfend
ms.date: 12/12/2019
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
ms.openlocfilehash: b29302ffe534f2439519e57c6a6b8c94c1df8d62
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917144"
---
# <a name="IF">IF ER-aðgerð</a>

[!include [banner](../includes/banner.md)]

Aðgerðin `IF` skilar fyrsta tilgreinda gildinu ef tilgreinda skilyrðið er uppfyllt. Að öðrum kosti skilar hún öðru tilgreinda gildinu. Gildið sem er skilað getur verið gildi allra þeirra gagnagerða sem studdar eru.

## <a name="syntax"></a>Málskipun

```
IF (condition, first value, second value) as any of the supported data types
```

## <a name="arguments"></a>Frumbreytur

`condition`: *Boole-gildi*

Gild skilyrt segð sem verður að prófa.

`first value`: *Einhver af þeim gagnagerðum sem studdar eru*

Niðurstaðan sem er skilað ef skilyrðið er uppfyllt.

`second value`: *Einhver af þeim gagnagerðum sem studdar eru*

Niðurstaðan sem er skilað ef skilyrðið er ekki uppfyllt.

## <a name="return-values"></a>Skilagildi

*Einhver af þeim gagnagerðum sem studdar eru*

Gildið sem myndast við einhverja af þeim gagnategundum sem studdar eru.

## <a name="usage-notes"></a>Notkunarbréf

Frumbreyturnar `first value` og `second value` verða að vera tilgreindar með því að nota sömu gagnagerð. Undantekning er gerð á hönnunartíma ef gagnagerðir stilltra gilda passa ekki saman.

Ef fyrsta gildið og annað gildið eru gildi af gagnagerðinni *Gámur (skrá)* eða *Skáalisti* er niðurstaðan aðeins með reitina sem eru til í báðum gildum.

## <a name="example"></a>Dæmi

`IF (1=2, "condition is met", "condition is not met")` skilar strengnum **"condition is not met"**.

## <a name="additional-resources"></a>Frekari upplýsingar

[Rökvirkni](er-functions-category-logical.md)
