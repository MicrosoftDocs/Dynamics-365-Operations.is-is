---
title: NULLCONTAINER ER-aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin NULLCONTAINER í rafrænni skýrslugerð (ER) er notuð.
author: NickSelin
ms.date: 12/12/2019
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
ms.openlocfilehash: 13159d9d7c8d1871886beb3cb1938ca8b0097e0efb6f10a9d1b229c49b9ff947
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6738577"
---
# <a name="nullcontainer-er-function"></a>NULLCONTAINER ER-aðgerð

[!include [banner](../includes/banner.md)]

Aðgerðin `NULLCONTAINER` skilar núll gildi fyrir *Ílát (skrá)* sem hefur sama skipulag og tilgreindur skráalisti eða skrá.

## <a name="syntax"></a>Málskipun

```vb
NULLCONTAINER (list)
```

## <a name="arguments"></a>Frumbreytur

`list`: *Skráalisti* eða *Ílát (skrá)*

Gild slóð hlutar í gagnagjafa af annaðhvort gerðinni *Skráalisti* eða *Gámur (skrá)*.

## <a name="return-values"></a>Skilagildi

*Gámur (skrá)*

Skráargildið sem verður til.

## <a name="usage-notes"></a>Notkunarbréf

> [!NOTE] 
> Þessi aðgerð er úrelt. Notaði aðgerðina `EMPTYRECORD` í staðinn. Frekari upplýsingar er að finna á [EMPTYRECORD](er-functions-record-emptyrecord.md).

## <a name="example"></a>Dæmi

`NULLCONTAINER (SPLIT ("abc", 1))` skilar nýrri tómri skrá sem hefur sömu uppbyggingu og listinn sem skilað er með `SPLIT`-aðgerðinni. Frekari upplýsingar er að finna á [SPLIT](er-functions-list-split.md).

## <a name="additional-resources"></a>Frekari upplýsingar

[Færsluvirkni](er-functions-category-record.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]