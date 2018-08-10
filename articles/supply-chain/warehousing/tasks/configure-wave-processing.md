--- 
title: Skilgreina bylgjuvinnslu
description: "Í þessum leiðbeiningum er lýst hvernig eigi að setja upp skilyrði sem ákvarða hvort bylgjur eru unnar handvirkt eða sjálfvirkt og vinnu sem er mynduð fyrir vöruhús þegar unnið er úr bylgju."
author: ShylaThompson
manager: AnnBe
ms.date: 06/07/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: f7a6db585468c235e07c4a0117a83995ec93f4b0
ms.contentlocale: is-is
ms.lasthandoff: 09/29/2017

---
# <a name="configure-wave-processing"></a>Skilgreina bylgjuvinnslu

[!include [task guide banner](../../includes/task-guide-banner.md)]

Í þessum leiðbeiningum er lýst hvernig eigi að setja upp skilyrði sem ákvarða hvort bylgjur eru unnar handvirkt eða sjálfvirkt og vinnu sem er mynduð fyrir vöruhús þegar unnið er úr bylgju. Tilgreina skal skilyrði með því að setja upp bylgjusniðmát og fyrirspurnir sem samsvara bylgju með losaðar línur í sölupantanir, framleiðslupantanir og kanban pantanir. Bylgjuvinnslu er notað í vöruhús sem nota aðgerðirnar í vöruhúsakerfiseiningunni og ekki þau sem nota aðgerðirnar í kerfinu birgðastjórnun. Hægt er að keyra þetta ferli fyrir sýnigögn fyrirtækisins USMF.

1. Fara í vöruhúsakerfi > Uppsetning > Bylgjur > bylgjusniðmát.
2. Smellið á „Nýtt“.
3. Í reitinn Heiti bylgjusniðmáts skal slá inn gildi.
    * Þegar sett er upp bylgjusniðmát er að tilgreina Röðina sem sniðmát eru samsvöruð við losuð lína á sölupantanir, framleiðslupantanir og kanbana. Þegar línu er losuð í vöruhús eða framleiðslu, notar hún fyrstu bylgjusniðmát sem hún uppfyllir skilyrði fyrir. Mælt er með því að setja sniðmát með nákvæmasta skilyrði efst á listanum. Því breiðara sem skilyrði er, því líklegra er fyrir línu til að uppfylla skilyrði, sem gæti leitt til að línur sé úthlutað á röng bylgju.  
4. Færa inn gildi í reitnum lýsingu bylgjusniðmáts.
5. Sláið inn eða veldu gildi í reitnum svæði.
    * Ef verið er að nota USMF er hægt að velja ‚svæði 2‘.  
6. Sláðu inn eða veldu gildi í reitnum Vöruhús.
    * Ef verið er að nota USMF er hægt að velja vöruhús 24.  
7. Svæðið stofnun bylgju sjálfvirk er stillt á Já.
    * Veljið þennan valkost til að stofna bylgju sjálfkrafa þegar sölupöntun, framleiðslupöntun eða kanban-losaðar í vöruhúsið.  
8. Stilla valkostinn fyrir Vinna úr bylgju við losun í vörugeymslu á já. 
    * Veljið þennan valkost til að vinna úr bylgjunni sjálfkrafa og stofna vinnu þegar lína er losuð í vöruhús.  
9. Kostur stofnun bylgju sjálfvirkt er stillt á Já. 
    * Veljið þennan valkost til að losa bylgju sjálfkrafa. Vinna tiltektarlista er stofnuð og í fartæki.  
10. Stilla valkostinn Úthluta á opnar bylgjur á Já. 
    * Línur eru úthlutað til bylgjur á grundvelli fyrirspurnarsía fyrir bylgjusniðmát.  
11. Setja vinna Úr bylgju sjálfkrafa við mörk kost á Já. 
    * Veljið þennan valkost til að vinna sjálfvirkt úr bylgjunni þegar hennar gildi nær þröskulda fyrir þyngd, sendingar, og línum sem tilgreind er í Bylgjuþröskuldum  svæðisflokknum. Þessi valkostur er bara tiltækur ef Senda er valinn í svæðinu Bylgjusniðmátsgerð.  
12. Kostur áfyllingarvinna sjálfvirkt er stillt á Já. 
    * Veljið þennan valkost til að stofna vinnu áfyllingar út frá eftirspurn og losa sjálfkrafa. Verður að bæta aðferð bylgju áfylling bylgjusniðmátið og stofna áfyllingarsniðmát af gerðinni Bylgjueftirspurn.  
13. Víkkið út hlutann aðferðir.
    * Aðferðir bylgjusniðmáts gera þér kleift að stýra röð verkþátta sem hver bylgja fer í gegnum þegar hún er unnin. Til dæmis gæti verið til aðferð fyrir áfyllingu bylgja . Þegar þú bætir við aðferð, er hún sjálfkrafa skráð í viðeigandi stað í röð af skrefum. Hafirðu stillt valkostinn útgefinn fyrir sjálfvirka áfyllingarvinnu á Já, þarftu að bæta við áfyllingarmáta hér.  
    * Bylgjueigindir virka sem síur til að takmarka þær vörur sem geta notað bylgjuna. Til dæmis gætir þú tilgreint flokkvöru.  
14. Smellið á „Vista“.
15. Lokið síðunni.
16. Fara í vöruhúsakerfi > Uppsetning > Færibreytur vöruhúsakerfis.
17. Útvíkka hlutann Úrvinnsla bylgju.
18. Færa inn eða velja gildi á svæði bylgjuúrvinnsla runuhóps
19. Stilla valkostinn Vinna bylgjur í runu á já.
20. Í reitinn bið eftir lás (ms) skal slá inn númer.
    * Færa inn þann tíma í millisekúndum sem úthlutun skref mun bíða þar til kerfið tilföng sem er læst af öðrum úthlutun skref. Þegar farið er yfir þennan tíma er ekki unnið úr bylgjunni og villuboð birtist.  
21. Smellið á „Vista“.
22. Lokið síðunni.
23. Smella skal á Framleiðslustýring > Uppsetningu >Færibreytur framleiðslustýringar.
24. Í reitnum losa í vöruhús skal velja valkost.
    * Fyrir sölupantanir og kanbanpantanir verður að taka frá birgðir áður en pöntun er losuð í vöruhús. Annars eru vörur eða úthlutunarlínur ekki hægt að vinna í bylgju. Fyrir framleiðslupantanir, er einnig sá kostur tiltækur að velja Leyfa hlutafrátekningu. Til dæmis, þetta er hentugt ef efnin sem þarf til að hefja framleiðslu eru til staðar og geta beðið þar til viðbótar efni verða tiltækar til að klára ferlið. Ef þessi valkostur er valinn verður handvirkt að endurtaka losun í vöruhúsaferli þegar viðbótar efni verða tiltækar.  
25. Lokið síðunni.


