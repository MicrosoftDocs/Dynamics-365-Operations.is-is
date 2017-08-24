--- 
title: "Skilgreina greiðsluskilmála lánardrottna"
description: "Setja upp greiðsluskilmála fyrir reikninga lánardrottins."
author: abruer
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: cbac3b27c25377abff341c4bf259e553c14a4ae8
ms.contentlocale: is-is
ms.lasthandoff: 07/27/2017

---
# <a name="define-vendor-payment-terms"></a>Skilgreina greiðsluskilmála lánardrottna

[!include[task guide banner](../../includes/task-guide-banner.md)]

Setja upp greiðsluskilmála fyrir reikninga lánardrottins. Þetta verkefni notar USMF-sýnifyrirtækið.

1. Fara í Viðskiptakröfur > Greiðsluuppsetning > Greiðsluskilmálar.
2. Smellið á „Nýtt“.
    * Skilmála greiðslu síða er notuð til að skilgreina hvernig verður að reikna út gjalddaga. Það er ekki notuð til að skilgreina hvernig dagsetning staðgreiðsluafsláttar reiknaðar.  
3. Færa inn gildi í svæðinu greiðsluskilmálar
4. Sláið inn gildi í reitnum „Lýsing“.
5. Í reitinn dagar skal slá inn númer.
    * Númerið sem fært er inn hér verður notað til að bæta við gjalddaga eða við lok tímabils sem skilgreind er í greiðsluaðferðina. Til dæmis, ef Nettó er valið, verður númerið bætt við gjalddaga. Ef valið er Gildandi mánuður, það bætir númeri bætt við síðasta dags núverandi mánaðar til að reikna út gjalddaga.  
6. Smellið á „Vista“.
7. Lokið síðunni.
8. Fara í Viðskiptakröfur > Greiðsluuppsetning > Staðgreiðsluafsláttur.
9. Smellið á „Nýtt“.
10. Færið inn Kenni í svæðinu staðgreiðsluafslátt.
11. Sláið inn gildi í reitnum „Lýsing“.
12. Ef lánardrottinn býður upp á lagskipt afslátt, velja næsta staðgreiðsluafsláttinn eftir að sá gildandi er útrunnið.
13. Lokið síðunni.
14. Í reitinn dagar skal slá inn númer.
    * Magnið sem er fært inn í svæðið Daga verður notuð til að reikna út dagsetningu staðgreiðsluafsláttar, á grundvelli hvaða valkostur var valinn í svæðinu Nettó/Gildandi. Ef Nettó var valinn er magn bætt við dagsetningu reiknings til að ákvarða dagsetningu staðgreiðsluafsláttar. Ef Núverandi mánuður var valinn er magn verður bætt við lok gjaldmiðilsmánaðar til að ákvarða dagsetningu staðgreiðsluafsláttar.  
15. Færið inn hlutfall staðgreiðsluafslátt í svæðinu Afsláttar. 
16. Færið inn aðallykils sem verður að staðgreiðsluafslátt verður bókaður fyrir reikninga viðskiptavina.
17. Færið inn aðallykils sem verður að bóka staðgreiðsluafslátt fyrir reikninga lánardrottins.
    * Ef 'Afsláttar mótlykils' er stillt til að Nota aðallykill fyrir afslátt lánardrottins, þá verður aðallykils notaður.  Ef valkosturinn er stillt á Lyklana á reikningslínum, verður staðgreiðsluafslátturinn bókaður á eignar/kostnaðarlykla í línum á reikningi.  
18. Smellið á „Vista“.


