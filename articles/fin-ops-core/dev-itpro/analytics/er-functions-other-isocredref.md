---
title: ISOCREDREF ER-aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin ISOCREDREF í rafrænni skýrslugerð (ER) er notuð.
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
ms.openlocfilehash: dd692720872314d533274f392f84e5ac7d36c7c1
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041378"
---
# <a name="ISOCREDREF">ISOCREDREF ER-aðgerð</a>

[!include [banner](../includes/banner.md)]

Aðgerðin `ISOCREDREF` skilar *strengja*-gildi sem sýnir tilvísun Alþjóðlegu staðlastofnunarinnar (ISO), byggt á tölustöfum og stafrófstáknum í tilgreindu númeri vörureiknings.

## <a name="syntax"></a>Málskipun

```vb
ISOCREDREF (invoice number digits)
```

## <a name="arguments"></a>Frumbreytur

`invoice number digits`: *Strengur*

Textagildi sem stendur fyrir tölustafi reikningsnúmers.

## <a name="return-values"></a>Skilagildi

*Strengur*

Textagildið sem verður til.

## <a name="usage-notes"></a>Notkunarbréf

> [!NOTE] 
> Til að útiloka tákn frá stafrófum sem ekki eru í samræmi við ISO skal frumbreytan `invoice number digits` þýdd áður en hún er sett inn í þessa aðgerð.

## <a name="example"></a>Dæmi

`ISOCredRef ("VEND-200002")` skilar **"RF23VEND-200002"**.

## <a name="additional-resources"></a>Frekari upplýsingar

[Other (lénsértæk virkni fyrir viðskipti)](er-functions-category-other.md)
