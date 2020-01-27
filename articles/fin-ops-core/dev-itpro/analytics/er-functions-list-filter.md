---
title: FILTER ER-aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin FILTER í rafrænni skýrslugerð (ER) er notuð.
author: NickSelin
manager: kfend
ms.date: 12/12/2019
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
ms.openlocfilehash: 2783fbfa0ba45c8d3772cf9ca16d110549d227b4
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917374"
---
# <a name="FILTER">FILTER ER-aðgerð</a>

[!include [banner](../includes/banner.md)]

Aðgerðin `FILTER` skilar tilgreindum lista sem *Skráalista*-gildi eftir að fyrirspurninni hefur verið breytt þannig að hún síar að tilteknu ástandi.

## <a name="syntax"></a>Málskipun

```
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

## <a name="usage-notes"></a>Notkunarbréf

Þessi aðgerð er frábrugðin [WHERE](er-functions-list-where.md) aðgerðinni, vegna þess að tilgreint skilyrði er beitt á hvaða gagnagjafa rafrænnar skýrslugerðar (ER) af gerðinni *Töflufærslur* á gagnagrunnsstigi. Listinn og forsendurnar er hægt að skilgreina með því að nota töflur og samskipti.

Ef ein eða báðar frumbreyturnar sem eru stilltar fyrir þessa aðgerð (`list` og `condition`) leyfa ekki að þýða þessa beiðni yfir í beint SQL-kall er gerð undantekning á hönnunartíma. Þessi undantekning upplýsir notandann um að ekki sé hægt að nota annaðhvort `list` eða `condition` til að spyrjast fyrir um gagnagrunninn.

## <a name="example-1"></a>Dæmi 1

Ef **Lánardrottinn** er stilltur sem ER-gagnagjafi sem vísar til VendTable-töflunnar skilar segðin `FILTER (Vendors, Vendors.VendGroup = "40")` lista yfir aðeins lánardrottna sem tilheyra lánardrottnaflokki 40.

## <a name="example-2"></a>Dæmi 2

Ef **Lánardrottinn** er stilltur sem ER-gagnagjafi sem vísar í VendTable-töfluna og ef **parmVendorBankGroup** er stillt sem ER-gagnagjafi sem skilar gildi af gagnagerðinni *Strengur* skilar segðin `FILTER ( Vendor.'<Relations'.VendBankAccount, Vendor.'<Relations'.VendBankAccount.BankGroupID = parmVendorBankGroup)` lista yfir aðeins lánardrottnalykla sem tilheyra tilteknum bankaflokk.

## <a name="example-3"></a>Dæmi 3

Þú slærð inn gagnagjafann **DS** af gerðinni *Reiknaður reitur* og hann inniheldur segðina `SPLIT ("A,B,C", ",")`. Síðan slærðu inn aðra segð, `FILTER( DS, DS.Value = "B")`. Þegar þú reynir að vista þessa segð í ER-formúluhönnuðinum er eftirfarandi undantekning gerð: "Staðfestingarvilla: Listasegðin í FILTER-aðgerð er ekki fyrirspurn."

## <a name="additional-resources"></a>Frekari upplýsingar

[Listavirkni](er-functions-category-list.md)
