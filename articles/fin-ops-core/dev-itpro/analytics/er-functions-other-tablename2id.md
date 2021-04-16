---
title: TABLENAME2ID ER-aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin TABLENAME2ID í rafrænni skýrslugerð (ER) er notuð.
author: NickSelin
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
ms.openlocfilehash: 0f94d00d9d40830d895e906ffbaa2a236f1efc43
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746556"
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