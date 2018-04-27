--- 
title: " Skilgreina vildarkerfi"
description: "Þetta ferli fer í gegnum hvernig á að skilgreina vildarkerfi."
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
ms.openlocfilehash: f398197566918c571128433c2fba3bf7d7c2fe3d
ms.contentlocale: is-is
ms.lasthandoff: 02/07/2018

---

# <a name="define-loyalty-schemes"></a> Skilgreina vildarkerfi

[!INCLUDE [task guide banner](../includes/task-guide-banner.md)]

Þetta ferli fer í gegnum hvernig á að skilgreina vildarkerfi. Vildarkerfi eru umbun og innleysingarreglur fyrir vildarkerfis. Þessi aðferð notar USRT sýnigögn fyrirtækisins.

1. Fara í Smásölu og viðskipti > Viðskiptamenn > Vild > vildarkerfi.
2. Smellið á „Nýtt“.
3. Færa inn gildi í reitnum Kenni skema .
4. Sláið inn gildi í reitnum „Lýsing“.
5. Í reitnum Heiti skal smella á fellilistahnappinn til að opna leitina.
    * Hægt er að hafa margar vildarkerfisáætlanir fyrir vildarkerfi. Vildarkerfi getur verið fyrir allar rásir miðlunarleiðir eða undirflokk rásar.  
6. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
7. Í listanum skal smella á tengilinn í valinni línu.
8. Smelltu á Vista.
9. Smellið á „Bæta við línu“.
10. Veljið valkost í svæðinu gerð verkþáttar.
    * Velja Innkaupaafurðir eftir upphæð ef óskað er eftir að viðskiptavinir ávinna umbun samkvæmt hversu mikið þær eyðslu. Velja Innkaupaafurðir eftir fjölda ef óskað er eftir að viðskiptavinir ávinna umbun samkvæmt hversu margar vörur þeir kaupa.  Veljið sölufærsla ef óskað er eftir að viðskiptavinir fái umbun fyrir hverja sölufærslur, óháð því hvaða eða hversu mikið er keypt.  
    * Veljið tegund. Tegund mun takmarka hvaða afurðir tekjuregla á við.  
    * Ef tekjuregla eiga við um allar afurðir er svæðið skilið eftir autt.  
11. Færið inn tölu í svæðinu upphæð aðgerðar/magn.
    *  Fyrir gerð verkþáttarins sölufærsla, alltaf ætti að nota í virðis '1,0'. Fyrir Verkþáttagerðir innkaupa eftir upphæð eða Innkaup eftir magni, fyrir færslur sem er minni en gildið sem fært er inn ekki virkjar ekki tekjuregla. Til dæmis, ef verkþáttargerð er innkaup með upphæð, og þú færa inn '10,00', síðan sölufærslu fyrir 9,00' þá fær það ekki umbun fyrir þessa tekjuregla.  
12. Í reitinn gjaldmiðill aðgerðar skal slá inn gildi.
13. Í reitnum Auðkenni vildarpunkts skal smella á fellilistahnappinn til að opna leitina.
14. Í listanum skal smella á tengilinn í valinni línu.
15. Í reitinn vildarpunktar skal slá inn númer.
    * Vildarpunktar af gerðinni Upphæð skráir áunna upphæð með aukastöfum. Til dæmis, ef tekjuregla tilgreinir 1 vildarpunktur fékkst fyrir hvert 1 kanadískur dalur eytt og viðskiptavinar eyðir 1.25 kanadískir dollarar þá ávinnur viðskiptavinar sér 1.25 vildarpunktar. Vildarpunktar af gerðinni fjöldi skráir áunna upphæð með heiltölum. Notum dæmið þar sem tekjuregla tilgreinir 1 vildarpunktur fékkst fyrir hvert 1 kanadískur dalur eytt og viðskiptavinar eyðir 1.25 kanadískir dollarar þá ávinnur viðskiptavinar sér 1.0 vildarpunktar.  
16. Smellið á „Vista“.
17. Smellið á „Bæta við línu“.
    * Innlausnarreglur eru notaðir þegar vildargreiðsluháttur sem er notuð.  
18. Í reitnum Auðkenni vildarpunkts skal smella á fellilistahnappinn til að opna leitina.
    * Aðeins innleysanlega vildarpunkta eru sýndar.  
19. Í listanum skal smella á tengilinn í valinni línu.
20. Í reitinn vildarpunktar skal slá inn númer.
21. Veljið valkost í svæðinu gerð innlausnar .
    * Að velja greiðslu eftir fjölda veldur því að Upphæð eða magni svæðið er farið með sem gjaldmiðilsgildi. Í þessu tilfelli er upphæð vildarpunktar notaðir á einingu í gjaldmiðli fasta hlutfall. Að velja greiðslu eftir fjölda veldur því að magn eða fjölda svæðið er farið með sem fjöldagildi. Í þessu tilfelli upphæð vildarpunktar sem nota á per magn vara er föst hlutfall, hins vegar getur upphæð í gjaldmiðli verið mismunandi ef verð vara greitt með vildarpunkta breytileg fyrir sama magn. Innlausnargerð punktar Vildarkerfis gildir aðeins 'Rússland' háðir Landi/Svæði er virkjað og virkniforstilling Sölustaðar hefur iso-kóðann 'RU'.  
    * Veljið tegund. Tegund mun takmarka hvaða afurðir innlausnarregla á við.  
    * Ef innlausnarregla eiga við um allar afurðir er svæðið skilið eftir autt.  
22. Færið inn tölu í reitnum Upphæð eða magn.
23. Í reitinn Gjaldmiðill skal slá inn gildi.
24. Smellið á „Vista“.
25. Smellið á „Bæta við línu“.
    * Velja einn eða fleiri hnúta úr Tiltækum fyrirtækishnútur og flytja þær í lista fyrirtækishnúts með því að smella á örina milli tveggja lista.  
26. Smellið á „Í lagi“.
27. Smellið á „Vista“.
    * Hvenær sem þú breytir rásir fyrir vildarkerfi er verður að keyra Vinnslu vildarkerfis. Þannig rásir verður að sækja uppfærðu vildarkerfi.  


