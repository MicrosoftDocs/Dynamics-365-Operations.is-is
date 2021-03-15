---
title: Stuðulafskrift
description: Þessi grein veitir yfirlit yfir stuðulsafskriftaraðferð.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: roschlom
ms.custom: 13831
ms.assetid: 2b6c4fe4-02ff-4191-bcad-32f1f34c15f2
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4920f7f90b859006ecdcd486eaa9f4449442e51a
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "4976142"
---
# <a name="factor-depreciation"></a>Stuðulafskrift

[!include [banner](../includes/banner.md)]

Þessi grein veitir yfirlit yfir stuðulsafskriftaraðferð.

Stuðlar eru prósenturnar sem eru notaðar til að afskrifa eignir. Þegar afskriftaregla fyrir eignir hefur verið sett upp og velur **þáttur** í **aðferð** svæðinu í síðunni **afskriftarregla** er hægt að setja upp stighækkandi, stiglækkandi eða línulega afskrift:

-   Í stighækkandi afskrift hækkar afskriftarupphæðin með hverju afskriftartímabili.
-   Í stiglækkandi afskrift lækkar afskriftarupphæðin á tímabili með tímanum.
-   Í línuleg afskrift eru afskriftirnar eins á hverju tímabili.

Reglurnar og dæmin að sem fylgja gefa til kynna hvernig hægt er að setja upp stuðla fyrir hverja gerð afskriftar. 

> [!NOTE] 
> Þegar þú velur **stuðull** í **aðferð** svæði, eru **stuðull** svæði og **Tímabil** svæði birt.

## <a name="progressive-depreciation"></a>Stighækkandi afskriftir
Gildið í reitnum **stuðull** er hærri en **50**.

### <a name="example"></a>Dæmi

Kaupverð er 100.000, stuðull er 70, líftími er 10 ár, og afskrift hefst á 1. janúar. Afskriftarupphæð og upphæð bókaðs nettóvirði eru sýnd aðeins fyrir fyrstu sex ári líftímans.

| Ár | Tímabil      | Afskriftarupphæð | Upphæð bókaðs nettóvirðis |
|------|-------------|---------------------|-----------------------|
| 1    | 31. desember | 307,69              | 99.692,31             |
| 2    | 31. desember | 1.447,21            | 98.245,10             |
| 3    | 31. desember | 3.104,50            | 95.140,60             |
| 4    | 31. desember | 5.150,21            | 89.990,39             |
| 5    | 31. desember | 7.522,95            | 82.467,44             |
| 6    | 31. desember | 10.184,06           | 72.283,38             |

## <a name="digressive-depreciation"></a>Stiglækkandi afskriftir
Gildið í reitnum **stuðull** er lægri en **50**.

### <a name="example"></a>Dæmi

Kaupverð er 100.000, stuðull er 20, líftími er 10 ár, og afskrift hefst á 1. janúar. Afskriftarupphæð og upphæð bókaðs nettóvirði eru sýnd aðeins fyrir fyrstu sex ári líftímans.

| Ár | Tímabil      | Afskriftarupphæð | Upphæð bókaðs nettóvirðis |
|------|-------------|---------------------|-----------------------|
| 1    | 31. desember | 56.080,43           | 43.919,57             |
| 2    | 31. desember | 10.665,70           | 33.253,87             |
| 3    | 31. desember | 7.156,22            | 26,097.65             |
| 4    | 31. desember | 5.538,06            | 20.559,59             |
| 5    | 31. desember | 4.579,89            | 15.979,70             |
| 6    | 31. desember | 3.937,36            | 12.042,34             |

## <a name="straight-line-depreciation"></a>Línuleg afskrift
Gildið í reitnum **stuðull** er jafn **50**. Í þessu tilfelli eru afskriftirnar þær sömu á hverju tímabili og þú ættir að hugsa um áhrif þeirra gilda sem voru tilgreind í öðrum reitum, eins og lýst er í [línulegur líftími afskriftar](straight-line-service-life-depreciation.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]