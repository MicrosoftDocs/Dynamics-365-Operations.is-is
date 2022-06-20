---
title: FILTER ER-aðgerð
description: Þessi grein veitir upplýsingar um hvernig aðgerðin FILTER Rafræn skýrslugerð (ER) er notuð.
author: NickSelin
ms.date: 12/14/2021
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
ms.openlocfilehash: dfa4afdcfad8c1855a10e1fa37c36cc5b20682ef
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8884518"
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
> The`FILTER` fall hegðar sér öðruvísi en`WHERE` virka þegar [`VALUEIN`](er-functions-logical-valuein.md) fall er notað til að tilgreina valviðmið.
> 
> - Ef`VALUEIN` fall er notað í umfangi`WHERE` fall, og önnur rökin af`VALUEIN` vísar til gagnagjafa sem skilar engum færslum, Boolean *[Rangt](er-formula-supported-data-types-primitive.md#boolean)* metur það`VALUEIN` ávöxtun kemur til greina. Því tjáningin`WHERE(Vendors, VALUEIN(Vendors.VendGroup, VendGroups, VendGroups.VendGroup))` skilar engum söluaðilaskrám ef **VendGroups** gagnagjafi skilar engum færslum lánardrottinshóps.
> - Ef`VALUEIN` fall er notað í umfangi`FILTER` fall, og önnur rökin af`VALUEIN` vísar til gagnagjafa sem skilar engum færslum, Boolean *[Rangt](er-formula-supported-data-types-primitive.md#boolean)* metur það`VALUEIN` ávöxtun er hunsuð. Því tjáningin`FILTER(Vendors, VALUEIN(Vendors.VendGroup, VendGroups, VendGroups.VendGroup))` skilar öllum færslum söluaðila um **Söluaðilar** gagnagjafa, jafnvel þó að **VendGroups** gagnagjafi skilar engum færslum lánardrottinshóps.

## <a name="example-1"></a>Dæmi 1

Ef **Lánardrottinn** er stilltur sem ER-gagnagjafi sem vísar til VendTable-töflunnar skilar segðin `FILTER (Vendors, Vendors.VendGroup = "40")` lista yfir aðeins lánardrottna sem tilheyra lánardrottnaflokki 40.

## <a name="example-2"></a>Dæmi 2

Ef **Lánardrottinn** er stilltur sem ER-gagnagjafi sem vísar í VendTable-töfluna og ef **parmVendorBankGroup** er stillt sem ER-gagnagjafi sem skilar gildi af gagnagerðinni *Strengur* skilar segðin `FILTER ( Vendor.'<Relations'.VendBankAccount, Vendor.'<Relations'.VendBankAccount.BankGroupID = parmVendorBankGroup)` lista yfir aðeins lánardrottnalykla sem tilheyra tilteknum bankaflokk.

## <a name="example-3"></a>Dæmi 3

Þú slærð inn gagnagjafann **DS** af gerðinni *Reiknaður reitur* og hann inniheldur segðina `SPLIT ("A,B,C", ",")`. Síðan slærðu inn aðra segð, `FILTER( DS, DS.Value = "B")`. Þegar þú reynir að vista þessa segð í ER-formúluhönnuðinum er eftirfarandi undantekning gerð: "Staðfestingarvilla: Listasegðin í FILTER-aðgerð er ekki fyrirspurn."

## <a name="additional-resources"></a>Frekari upplýsingar

[Listavirkni](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
