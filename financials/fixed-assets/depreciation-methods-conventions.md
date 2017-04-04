---
title: "Afskriftaraðferðir og venjur"
description: "Þessi grein veitir yfirlit yfir afskriftarreglur og afskriftaraðferðir sem eru studdar af Microsoft Dynamics AX."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: AssetDepreciationProfile, AssetGroupBookSetup, AssetGroupDepBookSetup
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 3441
ms.assetid: 1d8267b1-86a8-44bf-8814-f56b5d45a0ae
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 8e89a57dda8f2d392483ed13c686ea97b74926b0
ms.openlocfilehash: 51c053e6c130d20258e02284d097431a18bb38cb
ms.lasthandoff: 03/31/2017


---

# <a name="depreciation-methods-and-conventions"></a>Afskriftaraðferðir og venjur

Þessi grein veitir yfirlit yfir afskriftarreglur og afskriftaraðferðir sem eru studdar af Microsoft Dynamics AX.

Hægt er að velja ýmsar afskriftaaðferðir og reglur. Tilgangur aðferðanna er að úthluta afskriftavirði eignarinnar á fjárhagstímabil. Afskriftavirði eignarinnar er kaupverðið að frádregnu hugsanlegu rýrnunarvirði. 

Ef afskriftareglur eru notaðar og síðustu dagsetningu afskriftakeyrslu eignar er breytt, sem veldur því síðan að nokkrum afskriftum er sleppt, gætu afskriftir síðasta árs verið meiri eða minni en áætlað var. Afskriftirnar eru leiðréttar eftir fjölda afskriftatímabila sem verða fyrir áhrifum af breytingunni á síðustu dagsetningu afskriftakeyrslu.

Til dæmis, ef  hálfsárs afskriftareglan hefur verið notuð í þrjú ár, eiga afskriftirnar sér stað yfir 3 1/2 ár. Ef síðustu dagsetningu afskriftakeyrslu þessa 3 1/2 árs var breytt, flytur síðasta afskriftaárið út fjölda tímabila sem urðu fyrir áhrifum. Ef dagsetningin er flutt um þrjá mánuði, hefur síðasta árið níu mánaða virði til afskrifta þegar alla jafna hefði verið sex mánaða virði til afskrifta.

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

 



<a name="see-also"></a>Sjá einnig
--------

[Fixed asset depreciation](fixed-asset-depreciation.md)

[Straight line service life depreciation](Straight-line-service-life-depreciation.md)

[Reducing balance depreciation](reduce-balance-depreciation.md)

[Manual depreciation](manual-depreciation.md)

[Factor depreciation](factor-depreciation.md)

[Consumption depreciation](consumption-depreciation.md)

[Straight line life remaining depreciation](straight-line-life-remaining-depreciation.md)

[125% bókfært virði afskrift](125-percent-reducing-balance-depreciation.md)

[150% bókfært virði afskrift](150-percent-reducing-balance-depreciation.md)

[175% bókfært virði afskrift](175-percent-reducing-balance-depreciation.md)

[200% bókfært virði afskrift](200-percent-reducing-balance-depreciation.md)


