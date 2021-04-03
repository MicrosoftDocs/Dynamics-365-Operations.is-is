---
title: VALUEINLARGE ER aðgerð
description: Í þessu efnisatriði er að finna upplýsingar um hvernig VALUEINLARGE rafræn skýrslugerðarvirkni er notuð.
author: NickSelin
manager: kfend
ms.date: 08/17/2020
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
ms.search.validFrom: 2020-08-01
ms.dyn365.ops.version: AX 10.0.14
ms.openlocfilehash: 1e35c695d697e0d0f42baeaf568548273f9d205b
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/09/2021
ms.locfileid: "5565809"
---
# <a name="valueinlarge-er-function"></a>VALUEINLARGE ER aðgerð

[!include [banner](../includes/banner.md)]

`VALUEINLARGE` virknin ákvarðar hvort tilgreindur innsláttur *Int64* eða *Heiltala* passar við hvaða gildi hlutar sem er í tilgreindum lista. Virknin skilar *Boolean* gildið **TRUE** ef tilgreindur innsláttur passar við niðurstöðurnar af því að keyra tilgreinda segð fyrir að minnsta kosti eina færslu. Að öðrum kosti skilar hún *Boolean* gildinu **FALSE**. Til að skilja muninn með aðgerðinni `VALUEIN` skal skoða [Athugasemdir um notkun](#usage_note) síðar í þessu efnisatriði.

## <a name="syntax"></a>Málskipun

```vb
VALUEINLARGE (input, list, list item expression)
```

## <a name="arguments"></a>Frumbreytur

`input`: *Reitur*

Gild slóð gagnauppruna af gerðinni *Færslulisti*. Gildi þessa hlutar verður jafnað.

`list`: *Skráalisti*

Gild slóð í gagnagjafa af gagnagerðinni *Skráalisti*.

`list item expression`: *Segð*

Gild skilyrðisbundið segð sem annaðhvort bendir á eða inniheldur stakan reit af tilgreindum lista sem á að nota við jöfnunina.

## <a name="return-values"></a>Skilagildi

*Boole*

*Boole*-gildið sem myndast.

## <a name=""></a><a name="usage_note">Notkunarbréf</a>

Þegar tilgreint ílag stendur fyrir *Int64* eða *heiltölu* gerð gagnaupprunaatriðis er tilgreint hvaða kall er tengt við beina SQL-segð, listanum er breytt í tímabundna SQL-töflu og samsvörun er framkvæmd í gagnagrunninum með því að framkvæma eina `EXISTS JOIN` fyrirspurn. Annars virkar aðgerðin eins og [`VALUEIN`](er-functions-logical-valuein.md) aðgerðin.

Þegar tilgreint inntak stendur fyrir gagnaupprunavöru sem er hönnuð sem önnur vara en *Int64* og *heiltala* kemur fram villa á hönnunarstigi sem upplýsir að aðgerðin `VALUEINLARGE` eigi ekki við um skilgreinda segð rafrænnar skýrslugerðar.

Þegar `VALUEINLARGE` aðgerðarsegð er keyrð og fleiri en ein tímabundin tafla er notuð fyrir umfang þessarar framkvæmdar, kemur upp villa í keyrslu.

## <a name="example"></a>Dæmi

Þú skilgreinir eftirfarandi gagnagjafa í líkanavörpun þinni:

- Gagnagjafinn **In** af gerðinni *Töfluskrár*.
    - Þessi gagnagjafi vísar í töfluna **Intrastat** .
    - Að sjálfgefnu er valkosturinn **Milli fyrirtækja** stilltur á **Nei**.
- **InMemory** gagnagjafi af gerðinni *Reiknaður reitur*.
    - Þessi gagnaveita inniheldur segðina `WHERE (In, In.Port <> "")`.
- **InFiltered** gagnagjafi af gerðinni *Reiknaður reitur*.
    - Þessi gagnaveita inniheldur segðina `FILTER (In, VALUEINLARGE(In.RecId, InMemory, InMemory.RecId)`.

Þegar gagnagjafi **InFiltered** er kallaður undir samhengi fyrirtækisins **DEMF** er ný tímabundin tafla stofnuð í forritsgagnagrunninum, samansafn færslna auðkenniskóða í minnislista eru færð inn í þessa töflu og eftirfarandi SQL-yfirlit er myndað til að skila síuðum færslum af töflunni **Intrastat** .

```xpp
SELECT … from Intrastat T1
WHERE ((T1.PARTITION=?) AND (T1.DATAAREAID IN (N'DEMF'))) AND
EXISTS (SELECT 'x' FROM tempdb."DBO".? T2 WHERE ((T2.PARTITION=?) AND (T1.RecId=T2.RecId)))
```

## <a name="additional-resources"></a>Frekari upplýsingar

[Rökfræðiaðgerðir](er-functions-category-logical.md)

[VALUEIN aðgerðir](er-functions-logical-valuein.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]