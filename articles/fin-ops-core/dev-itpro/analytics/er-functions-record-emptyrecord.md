---
title: EMPTYRECORD ER-aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin EMPTYRECORD í rafrænni skýrslugerð (ER) er notuð.
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
ms.openlocfilehash: 1cf23f11fa92adfb7a050efd9c68e80e1bee621f
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916891"
---
# <a name="EMPTYRECORD">EMPTYRECORD ER-aðgerð</a>

[!include [banner](../includes/banner.md)]

Aðgerðin `EMPTYRECORD` skilar núll gildi fyrir *Ílát (skrá)* sem hefur sama skipulag og tilgreindur skráalisti eða skrá.

## <a name="syntax"></a>Málskipun

```
EMPTYRECORD (list)
```

## <a name="arguments"></a>Frumbreytur

`list`: *Skráalisti* eða *Ílát (skrá)*

Gild slóð hlutar í gagnagjafa af annaðhvort gerðinni *Skráalisti* eða *Gámur (skrá)*.

## <a name="return-values"></a>Skilagildi

*Gámur (skrá)*

Skráargildið sem verður til.

## <a name="usage-notes"></a>Notkunarbréf

> [!NOTE] 
> Færsla núll er færsla þar sem allir reitir eru með tómt gildi. Tómt gildi er **0** (núll) fyrir tölur, tóman streng fyrir strengi og svo framvegis.

## <a name="example"></a>Dæmi

`EMPTYRECORD (SPLIT ("abc", 1))` skilar nýrri tómri skrá sem hefur sömu uppbyggingu og listinn sem skilað er með `SPLIT`-aðgerðinni. Frekari upplýsingar er að finna á [SPLIT](er-functions-list-split.md).

## <a name="additional-resources"></a>Frekari upplýsingar

[Færsluvirkni](er-functions-category-record.md)
