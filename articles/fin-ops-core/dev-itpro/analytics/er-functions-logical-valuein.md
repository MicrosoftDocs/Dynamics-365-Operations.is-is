---
title: VALUEIN ER-aðgerð
description: Í þessari grein er að finna upplýsingar um hvernig VALUEIN rafræn skýrslugerðarvirkni (ER) er notuð.
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
ms.openlocfilehash: 14c3d08ee3478b55593a3e473f9eb60f1bba0760
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9288139"
---
# <a name="valuein-er-function"></a>VALUEIN ER-aðgerð

[!include [banner](../includes/banner.md)]

Aðgerðin `VALUEIN` ákvarðar hvort tilgreint ílag passar við eitthvert gildi tilgreinds hlutar sem er í tilgreindum lista. Hún skilar *Boolean*-gildinu **TRUE** ef tilgreint inntak passar við niðurstöðu þess að keyra tiltekna segð fyrir að minnsta kosti eina skrá af tilgreindum lista. Að öðrum kosti skilar hún *Boolean* gildinu **FALSE**.

## <a name="syntax"></a>Málskipun

```vb
VALUEIN (input, list, list item expression)
```

## <a name="arguments"></a>Frumbreytur

`input`: *Reitur*

Gild slóð hlutar í gagnagjafa af gerðinni *Skráalisti*. Gildi þessa hlutar verður jafnað.

`list`: *Skráalisti*

Gild slóð í gagnagjafa af gagnagerðinni *Skráalisti*.

`list item expression`: *Boole-gildi*

Gild skilyrðisbundið segð sem annaðhvort bendir á eða inniheldur stakan reit af tilgreindum lista sem á að nota við jöfnunina.

## <a name="return-values"></a>Skilagildi

*Boole*

*Boole*-gildið sem myndast.

## <a name="usage-notes"></a>Notkunarbréf

Almennt er virknin `VALUEIN` þýdd yfir í sett af **OR** skilyrðum. Ef listinn yfir **EÐA** skilyrði er stór og hugsanlega er farið yfir samtals hámarkslengd SQL-skipunar, skal íhuga að nota aðgerðina [`VALUEINLARGE`](er-functions-logical-valueinlarge.md).

```vb
(input = list.item1.value) OR (input = list.item2.value) OR …
```

SQLÍ sumum tilvikum er hægt að þýða það yfir í SQL-skipun gagnagrunns með því að nota virkjann `EXISTS JOIN`.

> [!NOTE]
> Gildið sem `VALUEIN` aðgerðin skilar er [notað á annan hátt](er-functions-list-filter.md#usage-notes) eftir því hvort þessi aðgerð er notuð til að tilgreina valskilyrðið fyrir [`FILTER`](er-functions-list-filter.md) aðgerðina eða [`WHERE`](er-functions-list-where.md) aðgerðina.

## <a name="example-1"></a>Dæmi 1

Í líkanavörpuninni skilgreinirðu gagnagjafann **Lista** af gerðinni *Reiknaður reitur*. Þessi gagnaveita inniheldur segðina `SPLIT ("a,b,c", ",")`.

Þegar gagnagjafi er kallaður, ef hann hefur verið stilltur sem segðin `VALUEIN ("B", List, List.Value)` skilar hann **TRUE**. Í þessu tilviki er aðgerðin `VALUEIN` þýdd í eftirfarandi samstæðu af skilyrðum: `(("B" = "a") or ("B" = "b") or ("B" = "c"))`, þar sem `("B" = "b")` er jafnt og **TRUE**.

Þegar gagnagjafi er kallaður, ef hann hefur verið stilltur sem segðin `VALUEIN ("B", List, LEFT(List.Value, 0))` skilar hann **FALSE**. Í þessu tilviki er aðgerðin `VALUEIN` þýdd í eftirfarandi skilyrði: `("B" = "")` sem er ekki jafnt og **TRUE**.

Efri mörkin fyrir fjölda stafa í texta slíks ástands eru 32.768 stafir. Þess vegna ættir þú ekki að búa til gagnaveitur sem kunna að fara yfir þessi mörk við keyrslu. Ef farið er yfir mörkin mun forritið stöðvast og undantekning er gerð. Til dæmis getur þetta ástand komið fram ef gagnaveitan er skilgreind sem `WHERE (List1, VALUEIN (List1.ID, List2, List2.ID)` og listarnir **List1** og **List2** innihalda mikið magn af færslum.

Í sumum tilfellum er `VALUEIN` þýtt í gagnagrunnsstreng með því að nota `EXISTS JOIN` virknitáknið. Þessi hegðun kemur fram þegar [`FILTER`](er-functions-list-filter.md) virknin er notuð og eftirfarandi skilyrði eru uppfyllt:

- Slökkt er á valkostinum **ASK FOR QUERY** fyrir gagnagjafa aðgerðarinnar `VALUEIN` sem vísar til lista yfir skrár. Engum viðbótarskilyrðum verður beitt á þessum gagnaveitum meðan á keyrslu stendur.
- Engar faldaðar segðir eru stilltar fyrir gagnaveituna `VALUEIN` aðgerðina sem vísar til listans yfir skrár.
- Listaatriði `VALUEIN` aðgerðarinnar vísar til reitar af tilgreindri gagnaveitu, ekki til segðar eða aðferðar þeirrar gagnaveitu.

Íhugaðu að nota þennan valkost í staðinn fyrir [`WHERE`](er-functions-list-where.md) aðgerðina sem er lýst hér að framan í þessu dæmi.

## <a name="example-2"></a>Dæmi 2

Þú skilgreinir eftirfarandi gagnagjafa í líkanavörpun þinni:

- Gagnagjafinn **In** af gerðinni *Töfluskrár*. Þessi gagnagjafi vísar til Intrastat töflunnar.
- Gagnagjafinn **Port** af gerðinni *Töfluskrár*. Þessi gagnagjafi vísar til IntrastatPort töflunnar.

Þegar gagnaveita er kölluð sem hefur verið stillt sem segðin `FILTER (In, VALUEIN(In.Port, Port, Port.PortId)`, er eftirfarandi SQL-skipun sköpuð til að skila síuðum skrám af Intrastat töflunni.

```vb
select … from Intrastat
exists join TableId from IntrastatPort
where IntrastatPort.PortId = Intrastat.Port
```

Fyrir **dataAreaId** reiti er endanleg SQL-skipun mynduð með því að nota `IN` virknitákn.

## <a name="example-3"></a>Dæmi 3

Þú skilgreinir eftirfarandi gagnagjafa í líkanavörpun þinni:

- Gagnagjafinn **Le** af gerðinni *Reiknaður reitur*. Þessi gagnaveita inniheldur segðina `SPLIT ("DEMF,GBSI,USMF", ",")`.
- Gagnagjafinn **In** af gerðinni *Töfluskrár*. Þessi gagnaheimild vísar til Intrastat töflunnar og kveikt er á valkostinum **Á milli fyrirtækja** fyrir hana.

Þegar gagnaveita er kölluð sem hefur verið stillt sem segðin `FILTER (In, VALUEIN (In.dataAreaId, Le, Le.Value)`, inniheldur endanleg SQL-skipun eftirfarandi skilyrði:

```vb
Intrastat.dataAreaId IN ('DEMF', 'GBSI', 'USMF')
```

## <a name="additional-resources"></a>Frekari upplýsingar

[Rökfræðiaðgerðir](er-functions-category-logical.md)

[VALUEINLARGE aðgerðir](er-functions-logical-valueinlarge.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
