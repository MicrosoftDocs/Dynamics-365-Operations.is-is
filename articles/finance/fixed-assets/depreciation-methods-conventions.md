---
title: Afskriftaraðferðir og venjur
description: Þessi grein veitir yfirlit yfir afskriftarreglur og afskriftaraðferðir sem eru studdar af Microsoft Dynamics 365 Finance.
author: ShylaThompson
manager: AnnBe
ms.date: 04/25/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetDepreciationProfile, AssetGroupBookSetup, AssetGroupDepBookSetup
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 3441
ms.assetid: 1d8267b1-86a8-44bf-8814-f56b5d45a0ae
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c3370db28f551b5ce4a9b49342cb0c0b2f3945c0
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/06/2019
ms.locfileid: "2769501"
---
# <a name="depreciation-methods-and-conventions"></a>Afskriftaaðferðir og hefðir

[!include [banner](../includes/banner.md)]

Þessi grein veitir yfirlit yfir studdar afskriftarreglur og afskriftaraðferðir.

Hægt er að velja ýmsar afskriftaaðferðir og reglur. Tilgangur aðferðanna er að úthluta afskriftavirði eignarinnar á fjárhagstímabil. Afskriftavirði eignarinnar er kaupverðið að frádregnu hugsanlegu rýrnunarvirði. 

Ef afskriftareglur eru notaðar og síðustu dagsetningu afskriftakeyrslu eignar er breytt, sem veldur því síðan að nokkrum afskriftum er sleppt, gætu afskriftir síðasta árs verið meiri eða minni en áætlað var. Afskriftirnar eru leiðréttar eftir fjölda afskriftatímabila sem verða fyrir áhrifum af breytingunni á síðustu dagsetningu afskriftakeyrslu.

Til dæmis, ef hálfsárs afskriftareglan hefur verið notuð í þrjú ár, eiga afskriftirnar sér stað yfir 3 1/2 ár. Ef síðustu dagsetningu afskriftakeyrslu þessa 3 1/2 árs var breytt, flytur síðasta afskriftaárið út fjölda tímabila sem urðu fyrir áhrifum. Ef dagsetningin er flutt um þrjá mánuði, hefur síðasta árið níu mánaða virði til afskrifta þegar alla jafna hefði verið sex mánaða virði til afskrifta.

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
-   Beinskiptur
-   Stuðull
-   Notkun
-   Línuleg á eftirstöðvum líftíma
-   200% bókfært virði
-   175% bókfært virði
-   150% bókfært virði
-   125% bókfært virði





<a name="additional-resources"></a>Frekari upplýsingar
--------

[Afskriftir eigna](fixed-asset-depreciation.md)

[Línuleg afskrift líftíma](Straight-line-service-life-depreciation.md)

[Afskrift lækkandi stöðu](reduce-balance-depreciation.md)

[Handvirkar afskriftir](manual-depreciation.md)

[Afskrift stuðuls](factor-depreciation.md)

[Notkunarafskrift](consumption-depreciation.md)

[Línuleg afskrift eftirstandandi líftíma](straight-line-life-remaining-depreciation.md)

[Afskriftir fyrir 125% bókfært virði](125-percent-reducing-balance-depreciation.md)

[Afskriftir fyrir 150% bókfært virði](150-percent-reducing-balance-depreciation.md)

[Afskriftir fyrir 175% bókfært virði](175-percent-reducing-balance-depreciation.md)

[Afskriftir fyrir 200% bókfært virði](200-percent-reducing-balance-depreciation.md)



