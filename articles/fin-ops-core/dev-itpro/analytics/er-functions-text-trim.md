---
title: TRIM ER-aðgerð
description: Þessi grein veitir upplýsingar um hvernig TRIM rafræn skýrslugerð (ER) aðgerðin er notuð.
author: kfend
ms.date: 02/28/2022
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
ms.openlocfilehash: 95b8d2989d705c4998da0af8e683adf567edfe92
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9273099"
---
# <a name="trim-er-function"></a>TRIM ER-aðgerð

[!include [banner](../includes/banner.md)]

The`TRIM` fall skilar tilgreindum textastreng sem a *Strengur* Gildi á eftir flipa, vagnsskila, línustreymi og formstraumstöfum hefur verið skipt út fyrir eitt bilstaf, eftir að fremstu og aftari bil hafa verið stytt og eftir að mörg bil milli orða hafa verið fjarlægð.

## <a name="syntax"></a>Málskipun

```vb
TRIM (text)
```

## <a name="arguments"></a>Frumbreytur

`text`: *Strengur*

Gild slóð í gagnagjafa af gerðinni *Strengur*.

## <a name="return-values"></a>Skilagildi

*Strengur*

Textagildið sem verður til.

## <a name="usage-notes"></a>Notkunarbréf

Í sumum tilfellum gætirðu viljað stytta fremsta og aftan bil en kjósa að halda áfram að forsníða fyrir tilgreindan texta. Til dæmis, þegar þessi texti táknar heimilisfang sem hægt væri að slá inn í marglínu textareitinn og gæti innihaldið línustraum og flutningsskilasnið. Í þessu tilviki skaltu nota eftirfarandi orðatiltæki:`REPLACE(text,"^[ \t]+|[ \t]+$","", true)` hvar`text` er röksemdin sem vísar til tilgreinds textastrengs.

## <a name="example-1"></a>Dæmi 1

`TRIM ("`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`Sample`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`text`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`")` skilar **"Sample text"**.

## <a name="example-2"></a>Dæmi 2

`TRIM (CONCATENATE (CHAR(10), "`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`Sample`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`", CHAR(9),"`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`text`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`", CHAR(13)))` skilar **"Dæmi um texta"**.

## <a name="additional-resources"></a>Frekari upplýsingar

[Textaaðgerðir](er-functions-category-text.md)

[REPLACE ER-aðgerð](er-functions-text-replace.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
