---
title: TRIM ER-aðgerð
description: Í þessari grein er að finna upplýsingar um hvernig TRIM rafræn skýrslugerðarvirkni (ER) er notuð.
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
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9273099"
---
# <a name="trim-er-function"></a>TRIM ER-aðgerð

[!include [banner](../includes/banner.md)]

`TRIM`-fallið skilar tilgreindum textastreng sem *Strengur*-gildi á eftir flipa, vendingu, línubil og síðuskiptastafi sem hefur verið skipt út fyrir eitt stafabilstákn eftir að bilum fyrir framan og aftan hefur verið eytt, og eftir að samfelld bil milli orðanna hafa verið fjarlægð.

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

Í sumum tilfellum gæti verið gott að stytta bil fyrir framan og aftan, en halda sniðinu fyrir tiltekinn texta. Þegar þessi texti sýnir til dæmis aðsetur sem gæti verið fært inn í textahólf með mörgum línum og gæti innihaldið línubil og vendingu. Í þessu tilfelli skaltu nota eftirfarandi segð: `REPLACE(text,"^[ \t]+|[ \t]+$","", true)` where `text` er frumbreytan sem vísar í tilgreindan textastreng.

## <a name="example-1"></a>Dæmi 1

`TRIM ("`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`Sample`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`text`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`")` skilar **"Sample text"**.

## <a name="example-2"></a>Dæmi 2

`TRIM (CONCATENATE (CHAR(10), "`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`Sample`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`", CHAR(9),"`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`text`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`", CHAR(13)))` skilar **"Sample text"**.

## <a name="additional-resources"></a>Frekari upplýsingar

[Textaaðgerðir](er-functions-category-text.md)

[REPLACE ER-aðgerð](er-functions-text-replace.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
