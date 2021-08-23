---
title: SUMIF ER aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin SUMIF í rafrænni skýrslugerð (ER) er notuð.
author: NickSelin
ms.date: 04/27/2020
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
ms.openlocfilehash: 8721e0115ab3c5ebe3071fe0b9ca5a80db766b0878d886b186f3f3d39f4a6397
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6747618"
---
# <a name="sumif-er-function"></a>SUMIF ER aðgerð

[!include [banner](../includes/banner.md)]

Aðgerðin `SUMIF` skilar *Raungildi* sem táknar summu gilda sem var skilað af bindingum sniðaþátta og safnað þegar sniðþættirnir voru notaðir til að búa til útleiðarskjal við sniðkeyrsluna og sem fullnægir tilgreindu skilyrði. Skilyrðið samanstendur af lykilsviði og lykilgildi.

## <a name="syntax"></a>Málskipun

```vb
SUMIF (key name for summing, condition range, condition value)
```

## <a name="arguments"></a>Frumbreytur

`key name for summing`: *Strengur*

Gildi sem er skilað með tjáningunni sem hefur verið stillt í eiginleikanum **Heiti lykils fyrir söfnuð gögn** í sniðhluta rafrænnar skýrslugerðar (ER) sem nota verður gildi bindingarinnar fyrir í samanburðarskyni.

Eiginleikann **Gildi lykils fyrir söfnuð gögn** er hægt að stilla fyrir annaðhvort íhlutinn **Röð** eða íhlutinn **XML-þáttur** í ER-sniði sem er að finna undir íhlutnum **Common\\File** þar sem kveikt er á valkostium **Safna saman upplýsingum um framleiðslu**.

## <a name="return-values"></a>Skilagildi

*Rauntala*

Tölugildið sem verður til.

## <a name="usage-notes"></a>Notkunarbréf

Þessi aðgerð skilar gildinu **0** (núll) þegar slökkt er á valkostinum **Safna saman upplýsingum um framleiðslu** í gildandi íhlutnum **Common\\File**.

Í frumbreytunni `condition range` er hægt að nota algildisstafinn **"\*"** til að tákna hvaða marga stafi sem er.

Í frumbreytunni `condition value` er hægt að nota algildisstafinn **"\*"** til að tákna hvaða marga stafi sem er.

## <a name="example"></a>Dæmi

Nánari upplýsingar um hvernig á að nota þessa aðgerð er að finna í [Rafræn skýrslugerð nota gögn sniðúttaks til að telja og leggja saman](tasks/er-format-counting-summing-1.md) leiðarvísir, sem er hluti af **Veita/þróa IT þjónustu/þáttum** viðskiptaferli.

Frekari upplýsingar og dæmi um notkun þessarar aðgerðar er að finna í [Keyrslu raðeininga í sniði rafrænnar skýrslugerðar fresta](er-defer-sequence-element.md#Example) og [Keyrslu XML-eininga í sniði rafrænnar skýrslugerðar frestað](er-defer-xml-element.md#Example).

## <a name="additional-resources"></a>Frekari upplýsingar

[Gagnasöfnunaraðgerðir](er-functions-category-data-collection.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]