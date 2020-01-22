---
title: GETCURRENTCOMPANY ER-aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin GETCURRENTCOMPANY í rafrænni skýrslugerð (ER) er notuð.
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
ms.openlocfilehash: a0b4c93a4705cd0e382b9b6c7af1d199beeceabe
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/20/2019
ms.locfileid: "2915994"
---
# <a name="GETCURRENTCOMPANY">GETCURRENTCOMPANY ER-aðgerð</a>

[!include [banner](../includes/banner.md)]

Aðgerðin `GETCURRENTCOMPANY` skilar *strengja*-gildi sem sýnir kóðann fyrir lögaðilann (fyrirtæki) sem notandi er skráður inn á.

## <a name="syntax"></a>Málskipun

```
GETCURRENTCOMPANY ()
```

## <a name="return-values"></a>Skilagildi

*Strengur*

Textagildið sem verður til.

## <a name="example"></a>Dæmi

`GETCURRENTCOMPANY ()` skilar **USMF** fyrir notanda sem er skráður inn á **Contoso Entertainment System USA** fyrirtæki.

## <a name="additional-resources"></a>Frekari upplýsingar

[Other (lénsértæk virkni fyrir viðskipti)](er-functions-category-other.md)
