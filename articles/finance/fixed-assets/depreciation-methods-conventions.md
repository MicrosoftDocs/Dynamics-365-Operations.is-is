---
title: Afskriftaraðferðir og venjur
description: Þessi grein veitir yfirlit yfir afskriftarreglur og afskriftaraðferðir sem eru studdar af Microsoft Dynamics 365 Finance.
author: moaamer
ms.date: 12/16/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetDepreciationProfile, AssetGroupBookSetup, AssetGroupDepBookSetup
audience: Application User
ms.reviewer: kfend
ms.custom: 3441
ms.assetid: 1d8267b1-86a8-44bf-8814-f56b5d45a0ae
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 066e571485602907d167b2ed1f7530b2285a02b6
ms.sourcegitcommit: d1683d033fc74adbc4465dd26f7b0055e7639753
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/05/2022
ms.locfileid: "8714174"
---
# <a name="depreciation-methods-and-conventions"></a>Afskriftaraðferðir og venjur

[!include [banner](../includes/banner.md)]

Þessi grein veitir yfirlit yfir studdar afskriftarreglur og afskriftaraðferðir.

Hægt er að velja ýmsar afskriftaaðferðir og reglur. Tilgangur aðferðanna er að úthluta afskriftavirði eignarinnar á fjárhagstímabil. Afskriftavirði eignarinnar er kaupverðið að frádregnu hugsanlegu rýrnunarvirði. 

Ef afskriftareglur eru notaðar og síðustu dagsetningu afskriftakeyrslu eignar er breytt, sem veldur því síðan að nokkrum afskriftum er sleppt, gætu afskriftir síðasta árs verið meiri eða minni en áætlað var. Afskriftirnar eru leiðréttar eftir fjölda afskriftatímabila sem verða fyrir áhrifum af breytingunni á síðustu dagsetningu afskriftakeyrslu.

Ef til dæmis hálfsárs afskriftareglan hefur verið notuð í þrjú ár eiga afskriftirnar sér stað yfir þrjú og hálft ár. Ef síðustu dagsetningu afskriftakeyrslu er breytt á þessu þremur og hálfu ári flytur síðasta afskriftaárið út fjölda tímabila sem urðu fyrir áhrifum. Ef dagsetningin er flutt um þrjá mánuði, hefur síðasta árið níu mánaða virði til afskrifta þegar alla jafna hefði verið sex mánaða virði til afskrifta.

Hægt er að velja úr eftirfarandi afskriftareglum.


-   Hálft ár
-   Heill mánuður
-   Miður fjórðungur
-   Miður mánuður (fyrsti mánaðar)
-   Miður mánuður (15. mánaðar)
-   Hálft ár (byrjun árs)
-   Hálft ár (næsta ár)

Hægt er að velja á milli eftirfarandi afskriftaraðferða.
-   Línuleg á líftíma
-   Bókfært virði
-   Handvirkt
-   Stuðull
-   Notkun
-   Línuleg á eftirstöðvum líftíma
-   200% bókfært virði
-   175% bókfært virði
-   150% bókfært virði
-   125% bókfært virði





## <a name="additional-resources"></a>Frekari upplýsingar

[Afskriftir eigna](fixed-asset-depreciation.md)

[Línulegar líftímaafskriftir](Straight-line-service-life-depreciation.md)

[Afskrift lækkandi stöðu](reduce-balance-depreciation.md)

[Handvirkar afskriftir](manual-depreciation.md)

[Afskrift stuðuls](factor-depreciation.md)

[Notkunarafskriftir](consumption-depreciation.md)

[Línuleg afskrift eftirstandandi líftíma](straight-line-life-remaining-depreciation.md)

[125 prósenta lækkandi afskrift](125-percent-reducing-balance-depreciation.md)

[Afskriftir fyrir 150% bókfært virði](150-percent-reducing-balance-depreciation.md)

[Afskriftir fyrir 175% bókfært virði](175-percent-reducing-balance-depreciation.md)

[Afskriftir fyrir 200% bókfært virði](200-percent-reducing-balance-depreciation.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
