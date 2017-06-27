---
title: "Áhrif afskrifta með bakfærslum"
description: "Þessi grein fjallar hugsanlega afleiðingar af því að bakfæra eignafærslu."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetTrans
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 2961
ms.assetid: 63a3ac92-c321-4379-a86a-b1b14915f340
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: d061ad8df477943259bff853d032c3df620e0b27
ms.contentlocale: is-is
ms.lasthandoff: 05/25/2017


---

# <a name="depreciation-effects-with-reversals"></a>Áhrif afskrifta með bakfærslum

[!include[banner](../includes/banner.md)]


Þessi grein fjallar hugsanlega afleiðingar af því að bakfæra eignafærslu. 

Hægt er að bakfæra eignafærslur og færslur sem tengjast eign. Einnig er hægt að afturkalla bakfærða færslu. 

Hægt er að bakfæra eða afturkalla færslu sem var ekki nýjasta færslan bókuð í bókina fyrir eignina. Fyrst að athuga hvort einhverjar afskriftafærslur voru bókaðar eftir færsluna sem á að bakfæra. Þetta er vegna þess að afskriftir eru ekki endurreiknaðar þegar færsla er bakfærð. Þess vegna verða afskriftir oft ýktar eða verða of litlar eftir bakfærsluna eins og sýnt er í dæmunum. 

Svo að tryggja megi að afskriftir séu réttar þegar færsla er bakfærð skal ekki halda áfram með bakfærsluna ef boð berast í ferlinu sem segja að afskriftir verði ekki endurreiknaðar. Í staðinn skal fyrst bakfæra afskriftarfærsluna sem var bókuð eftir færsluna sem reynt var að bakfæra og halda svo áfram með bakfærsluna. Þú verður ekki varaður við afskriftarútreikningum, og hægt er að halda áfram að bakfæra. 

Eftirfarandi dæmi sýna útreikninga sem eru gerðir ef valið er að halda áfram eftir viðvörunarboðin í stað þess að bakfæra fyrst afskriftarfærslurnar.

## <a name="example-1-depreciation-is-overstated"></a> Dæmi 1: Afskriftir eru ýktar
Eign er sett upp með 5 ára líftíma og línuleg afskrift (60 afskriftartímabil). Í þessu dæmi eru afskriftir ýktar.
#### <a name="asset-transaction-history"></a>Færslusaga eignar

| Dagsetning       | Færslugerð                                                          | Upphæð                                    |
|------------|---------------------------------------------------------------------------|-------------------------------------------|
| 1. janúar  | Kaup                                                               | 59.000,00                                 |
| 1. janúar  | Leiðrétting kaupa                                                    | 1.000,00                                  |
| 31. janúar | Afskrift (stofnuð með því að nota tillögu fyrir eitt afskriftartímabil) | 1,000.00Útreikningur: bókað virði (59.000 + 1.000) / Fjöldi afskriftartímabila sem er eftir (60) |

#### <a name="reversal-action"></a>Bakfærsluaðgerð

| Dagsetning      | Færslugerð                | Upphæð    |
|-----------|---------------------------------|-----------|
| 1. janúar | Bakfærsla leiðréttingar á eign | -1.000,00 |

#### <a name="depreciation-effect"></a>Áhrif afskriftar

| Dagsetning        | Færslugerð        | Upphæð                                                                                |
|-------------|-------------------------|---------------------------------------------------------------------------------------|
| 28. febrúar | Afskrift (tillaga) | 983.05Útreikningur: bókað virði (59.000 - 1.000 afskrift) / Fjöldi afskriftartímabila sem er eftir (59) |

Afskrift er ýkt um 16,95 (1000 - 983,.05).

## <a name="example-2-depreciation-is-understated"></a> Dæmi 2: Afskrift verður of lítil
Eign er sett upp með 5 ára líftíma og línuleg afskrift (60 afskriftartímabil). Í þessu dæmi eru afskriftir of litlar.
#### <a name="asset-transaction-history"></a>Færslusaga eigna

| Dagsetning       | Færslugerð                                                          | Upphæð                                      |
|------------|---------------------------------------------------------------------------|---------------------------------------------|
| 1. janúar  | Kaup                                                               | 59.000,00                                   |
| 1. janúar  | Leiðrétting niðurfærslu                                                     | 1.000,00                                    |
| 31. janúar | Afskrift (stofnuð með því að nota tillögu fyrir eitt afskriftartímabil) | 966.67Útreikningur: bókað virði (59.000 + 1.000) / Fjöldi afskriftartímabila sem er eftir (60) |

#### <a name="reversal-action"></a>Bakfærsluaðgerð

| Dagsetning      | Færslugerð               | Upphæð    |
|-----------|--------------------------------|-----------|
| 1. janúar | Leiðrétting Niðurfærslu bakfærð | -1.000,00 |

#### <a name="depreciation-effect"></a>Áhrif afskriftar

| Dagsetning        | Færslugerð        | Upphæð                                                                                       |
|-------------|-------------------------|----------------------------------------------------------------------------------------------|
| 28. febrúar | Afskrift (tillaga) | 983.62Útreikningur: bókað virði (59.000 + 966,67 afskrift) / Fjöldi afskriftartímabila sem er eftir (59) |

Afskrift er er höfð of lítil sem nemur 16,95 (983,62 - 966,67).



<a name="see-also"></a>Sjá einnig
--------

[Afskriftir eigna](fixed-asset-depreciation.md)




