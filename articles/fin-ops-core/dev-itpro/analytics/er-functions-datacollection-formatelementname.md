---
title: FORMATELEMENTNAME ER aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin FORMATELEMENTNAME í rafrænni skýrslugerð (ER) er notuð.
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
ms.openlocfilehash: f716fe779903b4e9142b7959d868256f2d84c624
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5755229"
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