---
title: CASE ER-aðgerð
description: Í þessari grein er að finna upplýsingar um hvernig CASE rafræn skýrslugerðarvirkni (ER) er notuð.
author: kfend
ms.date: 12/17/2019
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
ms.openlocfilehash: 702648e14abe980d246b92b0fe512bba07717e45
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9274860"
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
