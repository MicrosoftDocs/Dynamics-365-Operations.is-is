---
title: COUNTIFS ER aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin COUNTIFS í rafrænni skýrslugerð (ER) er notuð.
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
ms.openlocfilehash: 667002aa01537f846c616d38bba436da18f6e05f
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5755277"
---
# <a name="countifs-er-function"></a>COUNTIFS ER aðgerð

[!include [banner](../includes/banner.md)]

Aðgerðin `COUNTIFS` skilar *Heiltölu*-gildi sem táknar fjölda sniðaþátta sem var safnað þegar sniðþættirnir voru notaðir til að búa til útleiðarskjal við sniðkeyrsluna og sem fullnægir tilgreindum skilyrðum. Hvert skilyrði samanstendur af lykilsviði og lykilgildi.

## <a name="syntax"></a>Málskipun

```vb
COUNTIFS (condition 1 range, condition 1 value[, condition 2 range, condition 2 value, …, condition N range, condition N value])
```

## <a name="arguments"></a>Frumbreytur

`condition 1 range`: *Strengur*

Gildi sem er skilað með segðinni sem hefur verið stillt í eiginleikanum **Heiti lykils fyrir söfnuð gögn** í sniðsíhluta rafrænnar skýrslugerðar (ER). Þessi frumbreyta er skylda.

`condition 1 value`: *Strengur*

Gildi sem er skilað með segðinni sem hefur verið stillt í eiginleikanum **Gildi lykils fyrir söfnuð gögn** í ER-sniðsíhluta. Þessi frumbreyta er skylda.

`condition N range`: *Strengur*

Gildi sem er skilað með segðinni sem hefur verið stillt í eiginleikanum **Heiti lykils fyrir söfnuð gögn** í ER-sniðsíhluta. Þessar viðbótarfrumbreytur eru valkvæðar.

`condition N value`: *Strengur*

Gildi sem er skilað með segðinni sem hefur verið stillt í eiginleikanum **Gildi lykils fyrir söfnuð gögn** í ER-sniðsíhluta. Þessar viðbótarfrumbreytur eru valkvæðar.

## <a name="return-values"></a>Skilagildi

*Heiltala*

Tölugildið sem verður til.

## <a name="usage-notes"></a>Notkunarbréf

Eiginleikana **Heiti lykils fyrir söfnuð gögn** og **Gildi lykils fyrir söfnuð gögn** er hægt að stilla fyrir annaðhvort íhlutinn **Röð** eða íhlutinn **XML-þáttur** í ER-sniði sem er að finna undir íhlutnum **Common\\File** þar sem kveikt er á valkostinum **Safna saman upplýsingum um framleiðslu**.

Þessi aðgerð skilar gildinu **0** (núll) þegar slökkt er á valkostinum **Safna saman upplýsingum um framleiðslu** í gildandi íhlutnum **Common\\File**.

Í frumbreytunum `condition range` er hægt að nota algildisstafinn **"\*"** til að tákna hvaða marga stafi sem er.

Í frumbreytunum `condition value` er hægt að nota algildisstafinn **"\*"** til að tákna hvaða marga stafi sem er.

## <a name="example"></a>Dæmi

Nánari upplýsingar um hvernig á að nota þessa aðgerð er að finna í [Rafræn skýrslugerð nota gögn sniðúttaks til að telja og leggja saman](tasks/er-format-counting-summing-1.md) leiðarvísir, sem er hluti af **Veita/þróa IT þjónustu/þáttum** viðskiptaferli.

## <a name="additional-resources"></a>Frekari upplýsingar

[Gagnasöfnunaraðgerðir](er-functions-category-data-collection.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]