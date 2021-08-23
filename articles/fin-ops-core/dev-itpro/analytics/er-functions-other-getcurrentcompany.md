---
title: GETCURRENTCOMPANY ER-aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin GETCURRENTCOMPANY í rafrænni skýrslugerð (ER) er notuð.
author: NickSelin
ms.date: 12/17/2019
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
ms.openlocfilehash: c74ffaf1ee134da8d962e054656301d5e99827ff53f560f5d93f9dcb51819c13
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6760775"
---
# <a name="getcurrentcompany-er-function"></a>GETCURRENTCOMPANY ER-aðgerð

[!include [banner](../includes/banner.md)]

Aðgerðin `GETCURRENTCOMPANY` skilar *strengja*-gildi sem sýnir kóðann fyrir lögaðilann (fyrirtæki) sem notandi er skráður inn á.

## <a name="syntax"></a>Málskipun

```vb
GETCURRENTCOMPANY ()
```

## <a name="return-values"></a>Skilagildi

*Strengur*

Textagildið sem verður til.

## <a name="example"></a>Dæmi

`GETCURRENTCOMPANY ()` skilar **USMF** fyrir notanda sem er skráður inn á fyrirtækið **Contoso Entertainment System USA**.

## <a name="additional-resources"></a>Frekari upplýsingar

[Aðrar aðgerðir (fyrir fyrirtækislén)](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]