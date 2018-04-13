--- 
title: " Skilgreiningar verslunar fyrir smásöluyfirlit"
description: "Þetta ferli fer í gegnum skilgreiningar fyrir smásöluverslun sem hafa áhrif á hvernig smásöluuppgjör eru stofnuð og bókuð."
author: jashanno
manager: AnnBe
ms.date: 11/14/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: ea07d8e91c94d9fdad4c2d05533981e254420188
ms.openlocfilehash: 441ba692f559f9966f3e2512c7760ad2f732b768
ms.contentlocale: is-is
ms.lasthandoff: 02/07/2018

---
# <a name="store-configurations-for-retail-statements"></a> Skilgreiningar verslunar fyrir smásöluyfirlit

[!INCLUDE [task guide banner](../includes/task-guide-banner.md)]

Þetta ferli fer í gegnum skilgreiningar fyrir smásöluverslun sem hafa áhrif á hvernig smásöluuppgjör eru stofnuð og bókuð. Fjárhagsvíddir í smásöluverslunum eru til umfjöllunar í öðru ferli. Þessi aðferð notar sýnigögn USRT fyrirtækisins.

1. Fara í Smásölu og viðskipti > rásir > smásöluverslanir > allar smásöluverslanir.
2. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
3. Í listanum skal smella á tengilinn í valinni línu.
    * Stillingar í hlutanum Uppgjör/lokun hafa áhrif á stofnun yfirlits, villuleit og bókun fyrir verslunina.  Opna hlutann Uppgjör/lokun.  
    * Veljið aðferðina sem á að nota til að flokka línur yfirlits eftir.  
    * Veljið "Já" eigi aðeins að stofnað eitt uppgjör á dag þegar stofnað er yfirlits frá runuvinnslu stofnunar uppgjörs.  
    * útreikningssvæði fyrir talning skiptimyntar tilgreinir hvort talning skiptimyntar eigi að leggja saman eða hvort nota eigi það síðasta .  
    * Veljið fjárhagslykil til að bóka sléttunarmun í.  
    * Í svæðið Hámark sléttunarmismunar er hægt að færa inn hæstan leyfilegan sléttunarmismun.  
    * Í bókunarsvæðinu, er hægt að færa inn hámarkssamtala hámarksbókunarmismun leyfð fyrir yfirlit.  
    * Í svæðið Vakt er hægt að færa inn hámarks heildarmismunur á vakt innan yfirlits.  
    * Í svæðið færsla, er hægt að færa inn hámarks heildarmismunur í uppgjörslínu.  
    * Í svæðið aðferð Lokunar er hægt að skilgreina hvort færslur sem verða teknar með í uppgjör ætti að vera hluti af lokuð vakt eða hvort þau má hafa með í færslur innan marka skilgreinda dagsetning/tími.  
    * Í reitnum Lok viðskiptadags , er hægt að færa inn tíma ef bóka eigi færslur eftir miðnætti með fyrri dag.  
    * Veljið "Já" ef bóka eigi færslur eftir miðnætti sem hluti af fyrri dag.  
    * Veljið "Já" til að fá yfirlit sem stofnuð voru fyrir hverja uppgjörsaðferð sem var skilgreind. Þetta getur verið gagnlegt ef afköst við bókun þarf að vera endurbætt fyrir verslana með margar færslur, þar sem það stofnar mörg minni yfirlit sem má vinna samhliða.  
    * Í svæðinu Sjálfgefinn viðskiptavin hægt er að velja viðskiptavinalykillinn sem á að nota fyrir sölu til viðskiptavina sem koma af götunni.  


