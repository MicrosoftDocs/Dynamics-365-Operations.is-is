---
title: WEEKNUM ER-fall
description: Í þessari grein er að finna upplýsingar um hvernig WEEKNUM rafræn skýrslugerðarvirkni (ER) er notuð.
author: kfend
ms.date: 01/15/2022
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2021-12-03
ms.dyn365.ops.version: AX 10.0.24
ms.custom: 58771
ms.assetid: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
ms.openlocfilehash: 4658f88b7e353e651177fad0c8636c5403be1256
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9268147"
---
# <a name="weeknum-er-function"></a>WEEKNUM ER-fall

[!include [banner](../includes/banner.md)]

Aðgerðin `WEEKNUM` skilar *[Heiltölugildi](er-formula-supported-data-types-primitive.md#integer)* sem táknar viku ársins sem inniheldur tiltekið gildi fyrir *[Dagsetningu](er-formula-supported-data-types-primitive.md#date)*. Útreikningurinn byggist á menningarháðum reglum sem skilgreina almanaksviku og fyrsta dag vikunnar.

## <a name="syntax"></a>Málskipun

```vb
WEEKNUM (date, culture) as Integer
```

## <a name=""></a><a name="arguments">Frumbreytur</a>

`date`: *Dagsetning*

Dagsetningargildi sem táknar dagsetningu til að reikna viku ársins.

`culture`: *[Strengur](er-formula-supported-data-types-primitive.md#string)*

Menningin sem á að nota við útreikning. Hægt er að nota menningarkóða sem eru studdir í samræmi við .NET [staðla](/dotnet/api/system.globalization.cultureinfo.getcultures?view=net-5.0).

## <a name="return-values"></a>Skilagildi

*Heiltala*

Tölugildið sem verður til.

## <a name="usage-notes"></a>Notkunarbréf

Vikan á árinu er reiknuð út frá [ISO 8601](https://www.iso.org/iso-8601-date-and-time-format.html) staðlinum, ef staðallinn hefur verið samþykktur af landi eða svæði sem landsstaðallinn er gefinn upp fyrir við keyrslu. Annars er útreikningurinn byggður á lands-/svæðisbundnum landsstölum.

Ef óstuddur kóði [menningar](#arguments) er gefinn upp sem frumbreyta fyrir `WEEKNUM` aðgerðina við keyrslu er birt undantekning. Ef auði strengurinn er gefinn upp sem menningarkóði er enska dagatalið óháð landi notað til að reikna út vikunúmerið.

## <a name="examples"></a>Dæmi

`WEEKNUM (DATEVALUE ("01-01-2020", "de"))` skilar **1**.

`WEEKNUM (DATEVALUE ("01-01-2021", "de"))` skilar **53**.

`WEEKNUM (DATEVALUE ("01-01-2022", "de"))` skilar **52**.

`WEEKNUM (DATEVALUE ("01-01-2022", "ar"))` skilar **21**.

## <a name="additional-resources"></a>Frekari upplýsingar

[Dagsetningar- og tímaaðgerðir](er-functions-category-datetime.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
