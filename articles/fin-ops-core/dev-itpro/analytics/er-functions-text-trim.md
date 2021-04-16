---
title: TRIM ER-aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin TRIM í rafrænni skýrslugerð (ER) er notuð.
author: NickSelin
ms.date: 12/05/2019
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
ms.openlocfilehash: 93b08792a7aab7245d0443da05e0330bf8b2d56e
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746050"
---
# <a name="trim-er-function"></a>TRIM ER-aðgerð

[!include [banner](../includes/banner.md)]

Aðgerðin `TRIM` skilar tilgreindum textastreng sem *strengjagildi* eftir að bilum fyrir framan og aftan hefur verið eytt, og eftir að samfelld bil milli orðanna hafa verið fjarlægð.

## <a name="syntax"></a>Málskipun

```vb
TRIM (text )
```

## <a name="arguments"></a>Frumbreytur

`text`: *Strengur*

Gild slóð í gagnagjafa af gerðinni *Strengur*.

## <a name="return-values"></a>Skilagildi

*Strengur*

Textagildið sem verður til.

## <a name="example"></a>Dæmi

`TRIM ("`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`Sample`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`text`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`")` skilar **"Sample text"**.

## <a name="additional-resources"></a>Frekari upplýsingar

[Textavirkni](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]