---
title: ALLITEMS ER-aðgerð
description: Þessi grein veitir upplýsingar um hvernig ALLITEMS rafræn skýrslugerð (ER) aðgerðin er notuð.
author: NickSelin
ms.date: 12/04/2019
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
ms.openlocfilehash: d126f83c8bf5115917b676a57cf6527279ade462
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8864718"
---
# <a name="allitems-er-function"></a>ALLITEMS ER-aðgerð

[!include [banner](../includes/banner.md)]

Aðgerðin `ALLITEMS` keyrir sem val í minni og skilar nýju flöttu gildi *Skráalista* sem lista yfir skrár sem tákna alla hluti sem passa við tilgreinda slóð.

## <a name="syntax"></a>Málskipun

```vb
ALLITEMS (path)
```

## <a name="arguments"></a>Frumbreytur

`path`: *Skráalisti*

Gild slóð í gagnagjafa af gagnagerðinni *Skráalisti*.

## <a name="return-values"></a>Skilagildi

*Skráalisti*

Sá listi yfir skrár sem er búinn til.

## <a name="usage-notes"></a>Notkunarbréf

Slóðin verður að vera skilgreind sem gild slóð gagnagjafa á gagnagjafaþætti af gagnagerðinni *Skráalisti*. Gagnaeiningar eins og slóð strengs og dagsetning ætti að gefa upp villu í segðasmíði rafrænnar skýrslugerðar (ER) á tíma hönnunar.

Við mælum ekki með að þú notir þessa aðgerð fyrir færslugagnauppruna sem gætu innihaldið mikið magn gagna. Í staðinn skaltu íhuga að nota aðgerðina [ALLTEMSQUERY](er-functions-list-allitemsquery.md).

## <a name="example-1"></a>Dæmi 1

Ef þú slærð inn `SPLIT("abcdef" , 2)` sem gagnagjafa **DS** skilar segðin `COUNT( ALLITEMS (DS))` **3**.

## <a name="example-2"></a>Dæmi 2

Ef þú slærð inn **Vend** sem gagnagjafa gagnagerðarinnar *Skráalisti* sem vísar til jöfnunartöflunnar VendTable skilar segðin `ALLITEMS (Vend.'<Relations'.ContactPerson)` flötum lista yfir skrár sem eru með töfluskipulagið **ContactPerson** og innihalda alla tengiliði sem hægt er að opna með tengslunum **ContactPerson.ContactForParty == VendTable.Party** og eru tiltæk fyrir alla lánardrottna úr tilvísaðri lánardrottnatöflu.

## <a name="additional-resources"></a>Frekari upplýsingar

[Listavirkni](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]