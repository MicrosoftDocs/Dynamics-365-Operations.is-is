---
title: GETENUMVALUEBYNAME ER-aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin GETNUMVALUEBYNAME í rafrænni skýrslugerð (ER) er notuð.
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
ms.openlocfilehash: 33ccf358dc5355cd00d5ff41ebd8148a334cba38
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/01/2020
ms.locfileid: "3743856"
---
# <a name="getenumvaluebyname-er-function"></a>GETENUMVALUEBYNAME ER-aðgerð

[!include [banner](../includes/banner.md)]

Aðgerðin `GETENUMVALUEBYNAME` leitar að tilteknu *Enum*-gildi í tilgreindum tölusetningargagnagjafa með því að nota tölusetningarheitið sem er tilgreint sem *Strengja*-gildi. Ef *Enum*-gildi finnst skilar aðgerðin því. Að öðrum kosti skilar aðgerðin upptalningargildinu **núll**.

## <a name="syntax"></a>Málskipun

```vb
GETENUMVALUEBYNAME (enumeration data source path, enumeration value text)
```

## <a name="arguments"></a>Frumbreytur

`enumeration data source path`: *Upptalning*

Gild slóð gagnagjafa af einni af eftirfarandi upptalningargerðum:

- Líkanaupptalning rafrænnar skýrslugerðar (ER)
- Upptalning ER-sniðs
- Upptalning Microsoft Dynamics 365 Finance

`enumeration value text`: *Strengur*

Strengagildi sem táknar heiti staks upptalningargildis.

## <a name="return-values"></a>Skilagildi

Má vera núll *Enum*

Upptalningargildið sem myndast.

## <a name="usage-notes"></a>Notkunarbréf

Engin undantekning er gerð ef gildið *Enum* er ekki að finna með því að nota heiti upptalningargildisins sem er tilgreint sem gildið *Strengur*.

## <a name="example"></a>Dæmi

Í eftirfarandi mynd er **ReportDirection** upptalningin kynnt í gagnalíkani. Athugaðu að merki eru skilgreind fyrir tölusetningargildin.

<p><a href="./media/ER-data-model-enumeration-values.PNG"><img src="./media/ER-data-model-enumeration-values.PNG" alt="Available values for a data model enumeration" class="alignnone wp-image-290681 size-full" width="397" height="136" /></a>

Eftirfarandi mynd sýnir þessar upplýsingar:

- Gagnagjafinn **$Direction** er stilltur í ER-skýrslu. Þessi gagnagjafi er stilltur út frá líkanaupptalningunni **ReportDirection**.
- Segðin `$IsArrivals` er hönnuð til að nota líkanatölusetningarbyggðan gagnagjafa **$Direction** sem færibreytu þessarar aðgerðar.
- Gildi þessarar samanburðarsegðar er **TRUE**.

<a href="./media/ER-data-model-enumeration-usage.PNG"><img src="./media/ER-data-model-enumeration-usage.PNG" alt="Example of data model enumeration" class="alignnone wp-image-290681 size-full" width="397" height="136" /></a>

## <a name="additional-resources"></a>Frekari upplýsingar

[Textavirkni](er-functions-category-text.md)
