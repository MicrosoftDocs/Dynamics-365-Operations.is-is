---
title: TRANSLATE ER-aðgerð
description: Í þessari grein er að finna upplýsingar um hvernig TRANSLATE rafræn skýrslugerðarvirkni (ER) er notuð.
author: kfend
ms.date: 04/02/2020
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
ms.openlocfilehash: 7a15a28f6efa5333b54aa34938d22a9d6e404cec
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9278442"
---
# <a name="translate-er-function"></a>TRANSLATE ER-aðgerð

[!include [banner](../includes/banner.md)]

Aðgerðin `TRANSLATE` skilar gildinu *Strengur* sem inniheldur niðurstöðu þess að tilgreindum texta í stöfum er skipt út fyrir annað sett af stöfum.

## <a name="syntax"></a>Málskipun

```vb
TRANSLATE (text , pattern, replacement)
```

## <a name="arguments"></a>Frumbreytur

`text`: *Strengur*

Gild slóð í gagnagjafa af gerðinni *Strengur*.

`pattern`: *Strengur*

Textinn sem verður að skipta út.

`replacement`: *Strengur*

Textinn sem á að nota í staðinn.

## <a name="return-values"></a>Skilagildi

*Strengur*

Textagildið sem verður til.

## <a name="usage-notes"></a>Notkunarbréf

Aðgerðin `TRANSLATE` kemur í stað eins stafs í einu. Aðgerðin skiptir út fyrsta stafnum í frumbreytunni `text` með fyrsta stafnum í frumbreytunni `pattern` og síðan öðrum stafnum og fylgir sama flæði þar til að því er lokið. Þegar stafur úr frumbreytunum `text` og `pattern` stemmir er honum skipt út fyrir staf úr frumbreytunni `replacement` sem er staðsett í sömu stöðu og stafurinn úr frumbreytunni `pattern`. Ef stafur birtist margoft í frumbreytunni `pattern` er frumbreytuvörpunin `replacement` sem samsvarar fyrsta tilfelli þessa starfs notuð.

## <a name="example-1"></a>Dæmi 1

`TRANSLATE ("abcdef", "cd", "GH")` skiptir út stafnum **„c”** í tilteknum **„abcdef”** texta fyrir stafinn **„G”** í textanum `replacement` vegna eftirfarandi:
-   Stafurinn **„c”** er sýndur í textanum `pattern` í fyrstu stöðu.
-   Fyrsta staða textans `replacement` inniheldur stafinn **„G”**.

## <a name="example-2"></a>Dæmi 2

`TRANSLATE ("abcdef", "ccd", "GH")` skilar **„abGdef”**.

## <a name="example-3"></a>Dæmi 3

`TRANSLATE ("abccba", "abc", "123")` skilar **"123321"**.

## <a name="additional-resources"></a>Frekari upplýsingar

[Textaaðgerðir](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
