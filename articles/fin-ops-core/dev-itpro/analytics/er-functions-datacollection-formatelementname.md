---
title: FORMATELEMENTNAME ER aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin FORMATELEMENTNAME í rafrænni skýrslugerð (ER) er notuð.
author: NickSelin
manager: kfend
ms.date: 12/05/2019
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
ms.openlocfilehash: e8be55d9a90e841d64288b0c618c0012912ddbab
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/01/2020
ms.locfileid: "3745634"
---
# <a name="formatelementname-er-function"></a>FORMATELEMENTNAME ER aðgerð

[!include [banner](../includes/banner.md)]

Aðgerðin `FORMATELEMENTNAME` skilar *Strengja*-gildi sem táknar nafn á gildandi sniðmátsþætti rafrænnar skýrslugerðar (ER).

## <a name="syntax"></a>Málskipun

```vb
FORMATELEMENTNAME ()
```

## <a name="return-values"></a>Skilagildi

*Strengur*

Textagildið sem verður til.

## <a name="usage-notes"></a>Notkunarbréf

Þessa aðgerð er hægt að kalla í ER-segðum sem voru stilltar fyrir eiginleikana **Heiti lykils fyrir söfnuð gögn** og **Gildi lykils fyrir söfnuð gögn** í ER-sniðsíhlut úr hópnum **Texti** sem er að finna undir hlutanum **Common\\File** þar sem kveikt er á valkostinum **Safna saman upplýsingum um framleiðslu**.

## <a name="example"></a>Dæmi

Nánari upplýsingar um hvernig á að nota þessa aðgerð er að finna í [Rafræn skýrslugerð nota gögn sniðúttaks til að telja og leggja saman](tasks/er-format-counting-summing-1.md) leiðarvísir, sem er hluti af **Veita/þróa IT þjónustu/þáttum** viðskiptaferli.

## <a name="additional-resources"></a>Frekari upplýsingar

[Gagnasöfnunaraðgerðir](er-functions-category-data-collection.md)
