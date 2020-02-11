---
title: QRCODE ER-aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin QRCODE í rafrænni skýrslugerð (ER) er notuð.
author: NickSelin
manager: kfend
ms.date: 12/10/2019
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
ms.openlocfilehash: bac0910d213ee05a2a7a7b218a6714d4f935be16
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916753"
---
# <a name="QRCODE">QRCODE ER-aðgerð</a>

[!include [banner](../includes/banner.md)]

Aðgerðin `QRCODE` skilar *Íláts*-gildi sem sýnir Quick Response Code (QR-kóða) myndar fyrir tiltekinn streng á tvíundarsniði.

## <a name="syntax"></a>Málskipun

```
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

```
QRCODE (model.ListOfShelfLabels.LabelText)`
```

Þegar þú keyrir uppsett ER-snið er textagildið í reitnum **LabelText** í gagnagjafanum **model.ListOfShelfLabels** notað til að mynda mynd QR-kóða. Þessi mynd kemur í stað staðgengils fyrir mynd QR-kóða í skjalasniðmátinu sem er notað til að búa til skjal á útleið. Þegar þessi mynd af mynduðu skjali er skönnuð skilar hún textanum sem var tekinn úr reitnum **LabelText** í gagnagjafanum **model.ListOfShelfLabels**. Nánari upplýsingar er að finna í [Felldu inn myndir og form í skjöl sem þú myndar með því að nota ER](electronic-reporting-embed-images-shapes.md)

## <a name="additional-resources"></a>Frekari upplýsingar

[Textavirkni](er-functions-category-text.md)