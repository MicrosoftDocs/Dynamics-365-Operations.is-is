---
title: ENUMERATE ER-aðgerð
description: Þessi grein veitir upplýsingar um hvernig aðgerðin ENUMERATE Electronic Reporting (ER) er notuð.
author: NickSelin
ms.date: 12/12/2019
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
ms.openlocfilehash: 2ba0ab6ed3c1625904665d87f56745d9810ac782
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8891844"
---
# <a name="enumerate-er-function"></a>ENUMERATE ER-aðgerð

[!include [banner](../includes/banner.md)]

Aðgerðin `ENUMERATE` skilar nýju *Skráalista*-gildi sem samanstendur af tölusettum skrám á tilgreindum lista.

## <a name="syntax"></a>Málskipun

```vb
ENUMERATE (list)
```

## <a name="arguments"></a>Frumbreytur

`list`: *Skráalisti*

Gild slóð í gagnagjafa af gagnagerðinni *Skráalisti*.

## <a name="return-values"></a>Skilagildi

*Skráalisti*

Sá listi yfir skrár sem er búinn til.

## <a name="usage-notes"></a>Notkunarbréf

Listi yfir upptaldar skrár sem skilað er afhjúpar eftirfarandi viðbótarþætti:

- Skrá reitanna (íhlutinn **Gildi**)
- Gildandi færsluvísir (**Númer** þáttur)

## <a name="example"></a>Dæmi

Í eftirfarandi mynd er búinn til **Tölusettur** gagnagjafi sem tölusettur listi yfir færslur seljanda frá **Lánardrottnum** gagnagjafans sem vísar til VendTable töflunnar.

<a href="./media/picture-enumerate-datasource.jpg"><img src="./media/picture-enumerate-datasource.jpg" alt="Enumerated data source" class="alignnone wp-image-290711 size-full" width="387" height="136" /></a>

Eftirfarandi skýringarmynd sýnir snið rafrænnar skýrslugerðar (ER). Í þessu sniði eru gagnatengsl mynduð til að búa til úttak á XML sniði. Þetta úttak kynnir einstaka söluaðila sem upptalda hnúta.

<a href="./media/picture-enumerate-format.jpg"><img src="./media/picture-enumerate-format.jpg" alt="Format that has data bindings" class="alignnone wp-image-290721 size-full" width="414" height="138" /></a>

Eftirfarandi mynd sýnir niðurstöðuna þegar hannaða sniðið er keyrt.

<a href="./media/picture-enumerate-result.jpg"><img src="./media/picture-enumerate-result.jpg" alt="Result of running the format" class="alignnone wp-image-290731 size-full" width="567" height="176" /></a>

## <a name="additional-resources"></a>Frekari upplýsingar

[Listavirkni](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]