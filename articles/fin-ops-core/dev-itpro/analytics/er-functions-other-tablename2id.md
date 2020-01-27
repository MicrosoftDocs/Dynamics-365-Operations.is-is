---
title: TABLENAME2ID ER-aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin TABLENAME2ID í rafrænni skýrslugerð (ER) er notuð.
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
ms.openlocfilehash: 77d889f75f38b3c07855a96bf65f1456ac2f42e2
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/20/2019
ms.locfileid: "2915810"
---
# <a name="TABLENAME2ID">TABLENAME2ID ER aðgerð</a>

[!include [banner](../includes/banner.md)]

Aðgerðin `TABLENAME2ID` skilar tölulegri framsetningu töfluauðkennis fyrir tilgreint töfluheiti sem *heiltölu*-gildi.

## <a name="syntax"></a>Málskipun

```
TABLENAME2ID (text)
```

## <a name="arguments"></a>Frumbreytur

`text`: *Strengur*

Textagildi sem táknar gilt töfluheiti.

## <a name="return-values"></a>Skilagildi

*Heiltala*

Tölugildið sem verður til.

## <a name="usage-notes"></a>Notkunarbréf

Framkvæmd þessarar aðgerðar getur haft mismunandi niðurstöður í mismunandi tilvikum Microsoft Dynamics 365 Finance, jafnvel þó að sama fyrirtækisheiti sé notað.

## <a name="example"></a>Dæmi

`TABLENAME2ID ("Intrastat")` skilar **1510**.

## <a name="additional-resources"></a>Frekari upplýsingar

[Other (lénsértæk virkni fyrir viðskipti)](er-functions-category-other.md)
