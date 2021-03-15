---
title: Skilgreiningar verslunar fyrir smásöluyfirlit
description: Þetta ferli fer í gegnum skilgreiningar fyrir verslun sem hafa áhrif á hvernig uppgjör í Commerce eru stofnuð og bókuð.
author: jashanno
manager: AnnBe
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailStoreTable
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: af4321cd9d6e15c82c4eef1f1ca218b8301ebf35
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "5003654"
---
# <a name="store-configurations-for-retail-statements"></a>Skilgreiningar verslunar fyrir smásöluyfirlit

[!include [banner](../includes/banner.md)]

Þetta ferli fer í gegnum skilgreiningar fyrir verslun sem hafa áhrif á hvernig uppgjör í Commerce eru stofnuð og bókuð. Fjárhagsvíddir í verslunum eru til umfjöllunar í öðru ferli. Þessi aðferð notar sýnigögn USRT fyrirtækisins.

1. Í **Skoðunarrúðunni** ferðu í **Einingar > Retail og Commerce > Rásir > Verslanir > Allar smásöluverslanir**.
2. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
3. Í listanum skal smella á tengilinn í valinni línu.
4. Smellið á **Breyta**.
5. Stillingar í flýtiflipanum **Uppgjör/lokun** hafa áhrif á stofnun yfirlits, villuleit og bókun fyrir verslunina. Víkkið flýtiflipann **Uppgjör/lokun**.  
6. Í reitnum **Uppgjörsaðferð** skal velja aðferðina sem á að nota til að flokka línur yfirlits eftir.  
7. Veljið "Já" í **Eitt uppgjör á dag** eigi aðeins að stofna eitt uppgjör á dag þegar stofnað er yfirlits frá runuvinnslu stofnunar uppgjörs.  
8. Reiturinn **Útreikningur á talningu skiptimyntar** tilgreinir hvort talning skiptimyntar eigi að leggja saman eða hvort nota eigi það síðasta.  
9. Í reitnum **Sléttun** skal velja fjárhagslykil til að bóka sléttunarmun í.  
10. Í reitinn **Hámark sléttunarmismunar** er hægt að færa inn hæstan leyfilegan sléttunarmismun.
11. Í reitnum **Bókun** færirðu inn hámarkssamtölu bókunarmismunar sem er leyfð fyrir yfirlit.
12. Í reitnum **Vakt** skal færa inn hámarkssamtölu mismunar á vakt innan yfirlits.  
13. Í reitnum **Færsla** færirðu inn hámarkssamtölu mismunur í uppgjörslínu.  
14. Í reitnum **Lokunaraðferð** skilgreinirðu hvort færslur sem verða teknar með í uppgjör ætti að vera hluti af lokuð vakt eða hvort þau má hafa með í færslur innan marka skilgreinda dagsetning/tími.  
15. Í reitnum **Lok viðskiptadags** færirðu inn tíma ef bóka eigi færslur eftir miðnætti með deginum á undan.  
16. Veljið "Já" í **Bóka sem viðskiptadag** ef bóka skal færslur eftir miðnætti sem hluta af deginum á undan.  
17. Veljið "Já" í **Skipta eftir uppgjörsaðferð** til að fá yfirlit sem stofnuð voru fyrir hverja uppgjörsaðferð sem var skilgreind. Þessi aðgerð getur verið gagnleg ef afköst við bókun þarf að vera endurbætt fyrir verslana með margar færslur, þar sem það stofnar mörg minni yfirlit sem má vinna samhliða.  
18. Í flýtiflipanum **Almennt** í svæðinu **Sjálfgefinn viðskiptavinur** hægt er að velja viðskiptavinalykillinn sem á að nota fyrir sölu til viðskiptavina sem koma af götunni.  



[!INCLUDE[footer-include](../../includes/footer-banner.md)]