---
title: NUMERALSTOTEXT ER-aðgerð
description: Í þessari grein er að finna upplýsingar um hvernig NUMERALSTOTEXT rafræn skýrslugerðarvirkni (ER) er notuð.
author: kfend
ms.date: 12/10/2019
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
ms.openlocfilehash: 172693583699edfad7deeb16f8fc081abb6119d5
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9287989"
---
# <a name="numeralstotext-er-function"></a>NUMERALSTOTEXT ER-aðgerð

[!include [banner](../includes/banner.md)]

Aðgerðin `NUMERALSTOTEXT` skilar tilteknu tölunni sem *Strengja*-gildi eftir að það hefur verið stafsett (það er, breytt í textastrengi) á tilgreindu tungumáli.

## <a name="syntax"></a>Málskipun

```vb
NUMERALSTOTEXT (number, language, currency, print currency name flag, decimal points)
```

## <a name="arguments"></a>Frumbreytur

`number`: *Heiltala* eða *Raun*

Tölugildi sem tilgreinir töluna sem verður að stafa.

`language`: *Strengur*

Gildið *Strengur* sem táknar tungumálakóðann.

`currency`: *Strengur*

Gildið *Strengur* sem táknar gjaldmiðilskóðann.

`print currency name flag`: *Boole-gildi*

*Boolean*-gildi sem gefur til kynna hvort gjaldeyrisheiti verði að bæta við stafsetta textann.

`decimal points`: *Heiltala*

*Heiltölu*-gildi sem gefur til kynna fjölda aukastafa sem stafsettur texti ætti að hafa.

## <a name="return-values"></a>Skilagildi

*Strengur*

Textagildið sem verður til.

## <a name="usage-notes"></a>Notkunarbréf

Tungumálakóðinn er valfrjáls. Ef hann er skilgreindur sem tómur strengur er tungumálakóðinn fyrir samhengið sem er í keyrslu notaður. Sjálfgefinn tungumálakóði er **EN-US**. Tungumálakóðinn fyrir keyrandi samhengi er skilgreindur í þáttunum **möppu** eða **Skrá** í keyrandi sniði rafrænnar skýrslugerðar (ER).

Gjaldmiðilskóðinn er valkostur. Ef hann er skilgreindur sem tómur strengur er fyrirtækjagjaldmiðillinn fyrir samhengið sem er í keyrslu notaður.

> [!NOTE] 
> Frumbreyturnar `print currency name flag` og `decimal points` eru aðeins greindar fyrir eftirfarandi tungumálakóða: **CS**, **ET**, **HU**, **LT**, **LV**, **PL** og **RU**. Þar að auki er frumbreytan `print currency name flag` aðeins greind fyrir fyrirtæki þar sem samhengi landsins eða svæðisins styður frávik frá gjaldmiðlaheiti.

## <a name="example-1"></a>Dæmi 1

`NUMERALSTOTEXT (1234.56, "EN-US", "", false, 2)` skilar **"One Thousand Two Hundred Thirty Four and 56"**.

## <a name="example-2"></a>Dæmi 2

`NUMERALSTOTEXT (120, "PL", "", false, 0)` skilar **"Sto dwadzieścia"**. 

## <a name="example-3"></a>Dæmi 3

`NUMERALSTOTEXT (120.21, "RU", "EUR", true, 2)` skilar **"Сто двадцать евро 21 евроцент"**.

## <a name="additional-resources"></a>Frekari upplýsingar

[Textavirkni](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
