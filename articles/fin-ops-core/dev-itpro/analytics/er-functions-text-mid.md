---
title: MID ER-aðgerð
description: Þessi grein veitir upplýsingar um hvernig MID rafræn skýrslugerð (ER) aðgerðin er notuð.
author: NickSelin
ms.date: 12/10/2019
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
ms.openlocfilehash: ca5dbfb6de3057ad2c4a6dcc7ecce3d0ddc69595
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8867641"
---
# <a name="mid-er-function"></a>MID ER-aðgerð

[!include [banner](../includes/banner.md)]

Aðgerðin `MID` skilar *strengjagildi* sem sýnir tilgreindan fjölda staftákna frá tilteknum streng, með upphafi í tilgreindri stöðu.

## <a name="syntax"></a>Málskipun

```vb
MID (text, starting position, number of characters)
```

## <a name="arguments"></a>Frumbreytur

`text`: *Strengur*

Gildið *Strengur* sem tilgreinir textann sem á að skila staftáknum úr.

`starting position`: *Heiltala*

Gildið *Heiltala* sem tilgreinir staðsetningu fyrsta stafsins sem þarf að skila úr tilgreindum texta.

`number of characters`: *Heiltala*

Gildið *Heiltala* sem tilgreinir fjölda stafa sem þarf að skila, frá tilgreindri upphafsstöðu.

## <a name="return-values"></a>Skilagildi

*Strengur*

Textagildið sem verður til.

## <a name="usage-notes"></a>Notkunarbréf

Ef gildi frumbreytunnar `starting position` er lægra en 0 (núll) eru stafirnir sem er skilað taldir frá fyrstu stöðu í tilgreindum streng.

Ef gildi frumbreytunnar `starting position` er lengra en tilgreindur strengur er tómum streng skilað.

## <a name="example"></a>Dæmi

`MID ("Sample", 2, 3)` skilar **"amp"**.

## <a name="additional-resources"></a>Frekari upplýsingar

[Textavirkni](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]