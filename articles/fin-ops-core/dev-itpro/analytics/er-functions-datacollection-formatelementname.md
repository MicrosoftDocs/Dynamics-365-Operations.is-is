---
title: FORMATELEMENTNAME ER aðgerð
description: Þessi grein veitir upplýsingar um hvernig aðgerðin FORMATELEMENTNAME rafræn skýrslugerð (ER) er notuð.
author: kfend
ms.date: 12/05/2019
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
ms.openlocfilehash: 1c8c319075f8f39bec963df2c88d2d8d3beace43
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9275426"
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


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
