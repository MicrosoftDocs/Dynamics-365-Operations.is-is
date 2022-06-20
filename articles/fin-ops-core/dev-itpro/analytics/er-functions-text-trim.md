---
title: TRIM ER-aðgerð
description: Þessi grein veitir upplýsingar um hvernig TRIM rafræn skýrslugerð (ER) aðgerðin er notuð.
author: NickSelin
ms.date: 02/28/2022
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
ms.openlocfilehash: deadf89641771efa864e701af9dad57c5e62ea37
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8864645"
---
# <a name="trim-er-function"></a>TRIM ER-aðgerð

[!include [banner](../includes/banner.md)]

The`TRIM` fall skilar tilgreindum textastreng sem a *Strengur* Gildi á eftir flipa, vagnsskila, línustreymis og formstraumstöfum hefur verið skipt út fyrir eitt bilstaf, eftir að fremstu og aftari bil hafa verið stytt og eftir að mörg bil milli orða hafa verið fjarlægð.

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

Í sumum tilfellum gætirðu viljað stytta fremsta og aftan bil en kjósa að halda áfram að forsníða fyrir tilgreindan texta. Til dæmis, þegar þessi texti táknar heimilisfang sem hægt væri að slá inn í margra lína textareitinn og gæti innihaldið línustraum og flutningsskilasnið. Í þessu tilviki skaltu nota eftirfarandi orðatiltæki:`REPLACE(text,"^[ \t]+|[ \t]+$","", true)` hvar`text` er röksemdin sem vísar til tilgreinds textastrengs.

## <a name="example-1"></a>Dæmi 1

`TRIM ("`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`Sample`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`text`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`")` skilar **"Sample text"**.

## <a name="example-2"></a>Dæmi 2

`TRIM (CONCATENATE (CHAR(10), "`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`Sample`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`", CHAR(9),"`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`text`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`", CHAR(13)))` skilar **"Dæmi um texta"**.

## <a name="additional-resources"></a>Frekari upplýsingar

[Textaaðgerðir](er-functions-category-text.md)

[REPLACE ER-aðgerð](er-functions-text-replace.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
