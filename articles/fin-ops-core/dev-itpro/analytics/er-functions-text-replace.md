---
title: REPLACE ER-aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin REPLACE í rafrænni skýrslugerð (ER) er notuð.
author: NickSelin
manager: kfend
ms.date: 12/10/2019
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
ms.openlocfilehash: d9c66f4c96f35e3ad5fc92e7925b5cd07c956aac
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916868"
---
# <a name="REPLACE">REPLACE ER-aðgerð</a>

[!include [banner](../includes/banner.md)]

Aðgerðin `REPLACE` skilar tilgreindum textastreng sem *Strengja*-gildi eftir að öllu því eða öllu leyti hefur verið skipt út fyrir annan streng.

## <a name="syntax"></a>Málskipun

```
REPLACE (text, pattern, replacement, regular expression flag)
```

## <a name="arguments"></a>Frumbreytur

`text`: *Strengur*

Gild slóð í gagnagjafa af gerðinni *Strengur*.

`pattern`: *Strengur*

Ef frumbreytan `regular expression flag` er **FALSE** inniheldur þessi frumbreyta textann sem þarf að skipta um.

Ef frumbreytan `regular expression flag` er **TRUE** inniheldur þessi frumbreyta reglulega segð sem skilgreinir bæði leitarmynstur og uppbótatexta.

`replacement`: *Strengur*

Ef frumbreytan `regular expression flag` er **FALSE** inniheldur þessi frumbreyta textann sem á að nota til að skipta um.

Ef frumbreytan `regular expression flag` er **TRUE** er þessi frumbreyta ekki notuð.

`regular expression flag`: *Boole-gildi*

*Boolean*-gildi sem gefur til kynna hvort venjuleg segð sé notuð til að skipta um.

## <a name="return-values"></a>Skilagildi

*Strengur*

Textagildið sem verður til.

## <a name="usage-notes"></a>Notkunarbréf

Ef frumbreytan `regular expression flag` er **TRUE** skilar þessi aðgerð tilgreindum streng eftir að henni hefur verið breytt með því að beita venjulegu segð sem er tilgreind af frumbreytunni `pattern`. Reglulega segðin er notuð til að finna stafina sem verður að skipta út.

Ef frumbreytan `regular expression flag` er **FALSE** hagar þessi aðgerð sér eins og [TRANSLATE](er-functions-text-translate.md). Stafirnir sem eru tilgreindir af staðgengilsbreytunni `replacement` eru notaðir til að skipta út stöfum sem finnast. 

## <a name="example-1"></a>Dæmi 1

`REPLACE ("+1 923 456 4971", "[^0-9]", "", true)` notar reglulega segð sem fjarlægir öll tákn sem ekki eru tölur og skilar **"19234564971"**. 

## <a name="example-2"></a>Dæmi 2

`REPLACE ("abcdef", "cd", "GH", false)` kemur í stað mynstursins **"cd"** með strengnum **"GH"** og skilar **"abGHef"**.

## <a name="additional-resources"></a>Frekari upplýsingar

[Textavirkni](er-functions-category-text.md)