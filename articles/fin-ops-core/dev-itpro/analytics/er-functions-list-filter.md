---
title: FILTER ER-aðgerð
description: Í þessari grein er að finna upplýsingar um hvernig FILTER rafræn skýrslugerðarvirkni (ER) er notuð.
author: kfend
ms.date: 12/14/2021
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
ms.openlocfilehash: cfaf76daa8118942c3650e6b39c853434a20ee30
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9272589"
---
# <a name="filter-er-function"></a>FILTER ER-aðgerð

[!include [banner](../includes/banner.md)]

Aðgerðin `FILTER` skilar tilgreindum lista sem *Skráalista*-gildi eftir að fyrirspurninni hefur verið breytt þannig að hún síar að tilteknu ástandi.

## <a name="syntax"></a>Málskipun

```vb
FILTER (list, condition)
```

## <a name="arguments"></a>Frumbreytur

`list`: *Skráalisti*

Gild slóð í gagnagjafa af gagnagerðinni *Skráalisti*.

`condition`: *Boole-gildi*

Gild skilyrt tjáning sem er notuð til að sía skrár yfir tiltekinn lista.

## <a name="return-values"></a>Skilagildi

*Skráalisti*

Sá listi yfir skrár sem er búinn til.

## <a name="usage-notes"></a><a name="usage-notes"></a>Notkunarbréf

Þessi aðgerð er frábrugðin [WHERE](er-functions-list-where.md) aðgerðinni, vegna þess að tilgreint skilyrði er beitt á hvaða gagnagjafa rafrænnar skýrslugerðar (ER) af gerðinni *Töflufærslur* á gagnagrunnsstigi. Listinn og forsendurnar er hægt að skilgreina með því að nota töflur og samskipti.

Ef ein eða báðar frumbreyturnar sem eru stilltar fyrir þessa aðgerð (`list` og `condition`) leyfa ekki að þýða þessa beiðni yfir í beint SQL-kall er gerð undantekning á hönnunartíma. Þessi undantekning upplýsir notandann um að ekki sé hægt að nota annaðhvort `list` eða `condition` til að spyrjast fyrir um gagnagrunninn.

> [!NOTE]
> Aðgerðin `FILTER` hegðar sér á annan hátt en `WHERE` aðgerðina þegar [`VALUEIN`](er-functions-logical-valuein.md) virknin er notuð til að tilgreina valskilyrðin.
> 
> - Ef `VALUEIN` aðgerðina er notuð í umfangi `WHERE` aðgerðar og önnur frumbreyta `VALUEIN` vísar í gagnagjafa sem skilar engum færslur er Boole-gildið *[Ósatt](er-formula-supported-data-types-primitive.md#boolean)* sem skilar `VALUEIN` tekið til greina. Þar af leiðandi skilar segðin `WHERE(Vendors, VALUEIN(Vendors.VendGroup, VendGroups, VendGroups.VendGroup))` engum lánardrottnafærslum ef gagnagjafinn **VendGroups** skilar engum færslum lánardrottnaflokks.
> - Ef `VALUEIN` aðgerðina er notuð í umfangi `FILTER` aðgerðar og önnur frumbreyta `VALUEIN` vísar í gagnagjafa sem skilar engum færslur er Boole-gildið *[Ósatt](er-formula-supported-data-types-primitive.md#boolean)* sem skilar `VALUEIN` hunsað. Þar af leiðandi skilar segðin `FILTER(Vendors, VALUEIN(Vendors.VendGroup, VendGroups, VendGroups.VendGroup))` öllum lánardrottnafærslum fyrir gagnagjafann **Lánardrottnar** jafnvel þótt gagnagjafinn **VendGroups** skili engum færslum lánardrottnaflokks.

## <a name="example-1"></a>Dæmi 1

Ef **Lánardrottinn** er stilltur sem ER-gagnagjafi sem vísar til VendTable-töflunnar skilar segðin `FILTER (Vendors, Vendors.VendGroup = "40")` lista yfir aðeins lánardrottna sem tilheyra lánardrottnaflokki 40.

## <a name="example-2"></a>Dæmi 2

Ef **Lánardrottinn** er stilltur sem ER-gagnagjafi sem vísar í VendTable-töfluna og ef **parmVendorBankGroup** er stillt sem ER-gagnagjafi sem skilar gildi af gagnagerðinni *Strengur* skilar segðin `FILTER ( Vendor.'<Relations'.VendBankAccount, Vendor.'<Relations'.VendBankAccount.BankGroupID = parmVendorBankGroup)` lista yfir aðeins lánardrottnalykla sem tilheyra tilteknum bankaflokk.

## <a name="example-3"></a>Dæmi 3

Þú slærð inn gagnagjafann **DS** af gerðinni *Reiknaður reitur* og hann inniheldur segðina `SPLIT ("A,B,C", ",")`. Síðan slærðu inn aðra segð, `FILTER( DS, DS.Value = "B")`. Þegar þú reynir að vista þessa segð í ER-formúluhönnuðinum er eftirfarandi undantekning gerð: "Staðfestingarvilla: Listasegðin í FILTER-aðgerð er ekki fyrirspurn."

## <a name="additional-resources"></a>Frekari upplýsingar

[Listavirkni](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
