---
title: CASE ER-aðgerð
description: Þessi grein veitir upplýsingar um hvernig CASE rafræn skýrslugerð (ER) aðgerðin er notuð.
author: NickSelin
ms.date: 12/17/2019
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
ms.openlocfilehash: f8ce598315bfbf291fafc6c9c9d54133486fb352
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8854757"
---
# <a name="case-er-function"></a>CASE ER-aðgerð

[!include [banner](../includes/banner.md)]

Aðgerðin `CASE` metur gildi tiltekinnar segðar á móti tilgreindum valkostum og skilar niðurstöðu fyrsta valmöguleikans sem jafngildir gildi tiltekinnar segðar. Annars skilar hún valkvæðri sjálfgefinni niðurstöðu, ef sjálfgefin niðurstaða er tilgreind sem síðasta frumbreyta kallaðrar aðgerðar sem valkostur kemur ekki á undan. Gildið sem er skilað getur verið gildi allra þeirra gagnagerða sem studdar eru.

## <a name="syntax"></a>Málskipun

```vb
CASE (expression, option 1, result 1[, option 2, result 2, …, option N, result N, default result])
```

## <a name="arguments"></a>Frumbreytur

`expression`: *Frumstæð gagnagerð* (Boolean, tölulegt eða texti)

Gild segð sem skilar gildi frumstæðrar gagnagerðar.

`option 1`: *Frumstæð gagnagerð* (Boolean, tölulegt eða texti)

Gild segð sem skilar gildi sömu frumstæðu gagnagerðar og frumbreytan `expression` í kallaðri aðgerð. Þessi frumbreyta er áskilin.

`result 1`: *Einhver af þeim gagnagerðum sem studdar eru*

Niðurstaðan sem er skilað og samsvarar valkostinum á undan. Þessi frumbreyta er áskilin.

`option N`: *Frumstæð gagnagerð* (Boolean, tölulegt eða texti)

Gild segð sem skilar gildi sömu frumstæðu gagnagerðar og frumbreytan `expression` í kallaðri aðgerð. Þessi frumbreya er valfrjáls.

`result N`: *Einhver af þeim gagnagerðum sem studdar eru*

Niðurstaðan sem er skilað og samsvarar valkostinum á undan. Þessi frumbreya er valfrjáls.

`default result`: *Einhver af þeim gagnagerðum sem studdar eru*

Árangurinn sem ætti að vera skilað ef ekki er samsvörun. Þessi frumbreya er valfrjáls.

## <a name="return-values"></a>Skilagildi

*Einhver af þeim gagnagerðum sem studdar eru*

Gildið sem myndast við einhverja af þeim gagnategundum sem studdar eru.

## <a name="usage-notes"></a>Notkunarbréf

Undantekning er gerð þegar keyrslutími er ekki samsvarandi og valkvæð sjálfgefin niðurstaða er ekki skilgreind.

Tilgreina verður allar niðurstöður með sömu gagnagerð. Undantekning er gerð á hönnunartíma ef gagnagerðir stilltra niðurstaðna passa ekki saman.

Ef fyrsta niðurstöðugildið og *N*-ta niðurstöðugildið eru gildi af gagnagerðinni *Ílát (skrá)* eða *Skráalisti* er niðurstaðan aðeins með reitina sem eru til í báðum gildum.

## <a name="example"></a>Dæmi

`CASE( DATETIMEFORMAT( NOW(), "MM"), "10", "WINTER", "11", "WINTER", "12", "WINTER", "")` skilar strengnum **"WINTER"** ef gildandi setudagsetning forrits er á milli októbers og desembers. Annars skilar það auður strengur.

## <a name="additional-resources"></a>Frekari upplýsingar

[Rökvirkni](er-functions-category-logical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]