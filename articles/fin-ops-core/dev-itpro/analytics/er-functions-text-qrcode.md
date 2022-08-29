---
title: QRCODE ER-aðgerð
description: Þessi grein veitir upplýsingar um hvernig QRCODE rafræn skýrslugerð (ER) aðgerðin er notuð.
author: kfend
ms.date: 12/10/2019
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
ms.openlocfilehash: 9de62eefb82942ccc72e81bd9bf36eed07c99dba
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9287189"
---
# <a name="qrcode-er-function"></a>QRCODE ER-aðgerð

[!include [banner](../includes/banner.md)]

Aðgerðin `QRCODE` skilar *Íláts*-gildi sem sýnir Quick Response Code (QR-kóða) myndar fyrir tiltekinn streng á tvíundarsniði.

## <a name="syntax"></a>Málskipun

```vb
QRCODE (text)
```

## <a name="arguments"></a>Frumbreytur

`text`: *Strengur*

Gildið *Strengur* sem táknar upprunalega textann.

## <a name="return-values"></a>Skilagildi

*Hólf*

Tvíundarstraumurinn sem myndast.

## <a name="example"></a>Dæmi

Þú getur stillt rafræn skýrslugerð (ER) snið til að búa til útgagnaskjal í Microsoft Office snið (Excel-vinnubækur eða Word-skjöl) með því að nota fyrirfram skilgreint sniðmát. Þetta sniðmát getur innihaldið hlutinn **Mynd** (Excel-vinnubók) eða **Myndstjórnun** (Word-skjal) sem staðgengil fyrir mynd QR-kóða. Þú verður að bæta við stillt ER-snið þættinum **Hólf** sem verður notaður til að fylla inn í þennan staðgengil. Til að tilgreina hvaða upplýsingar verða geymdar í QR-kóða þarf að skilgreina bindingu fyrir þennan þátt **Hólf**. Til dæmis er hægt að stilla slíka bindingu sem inniheldur eftirfarandi segð:

```vb
QRCODE (model.ListOfShelfLabels.LabelText)`
```

Þegar þú keyrir uppsett ER-snið er textagildið í reitnum **LabelText** í gagnagjafanum **model.ListOfShelfLabels** notað til að mynda mynd QR-kóða. Þessi mynd kemur í stað staðgengils fyrir mynd QR-kóða í skjalasniðmátinu sem er notað til að búa til skjal á útleið. Þegar þessi mynd af mynduðu skjali er skönnuð skilar hún textanum sem var tekinn úr reitnum **LabelText** í gagnagjafanum **model.ListOfShelfLabels**. Nánari upplýsingar er að finna í [Felldu inn myndir og form í skjöl sem þú myndar með því að nota ER](electronic-reporting-embed-images-shapes.md)

## <a name="additional-resources"></a>Frekari upplýsingar

[Textavirkni](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
