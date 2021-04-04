---
title: TABLENAME2ID ER-aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin TABLENAME2ID í rafrænni skýrslugerð (ER) er notuð.
author: NickSelin
manager: kfend
ms.date: 12/12/2019
ms.topic: article
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
ms.openlocfilehash: 49370af4ebb7552dd3aff4512890fd93fa67c72d
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/09/2021
ms.locfileid: "5563271"
---
# <a name="tablename2id-er-function"></a>TABLENAME2ID ER-aðgerð

[!include [banner](../includes/banner.md)]

Aðgerðin `TABLENAME2ID` skilar tölulegri framsetningu töfluauðkennis fyrir tilgreint töfluheiti sem *heiltölu*-gildi.

## <a name="syntax"></a>Málskipun

```vb
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


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]