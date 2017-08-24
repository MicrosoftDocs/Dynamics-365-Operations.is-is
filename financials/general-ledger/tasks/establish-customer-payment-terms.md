--- 
title: "Setja greiðsluskilmála fyrir viðskiptavin"
description: "Þetta ferli skilgreinir staðgreiðsluafslátt og uppsetning gjalddaga."
author: aprilolson
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
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: c871421254be6b0e9443fdf596932776d64428ae
ms.contentlocale: is-is
ms.lasthandoff: 07/27/2017

---
# <a name="establish-customer-payment-terms"></a>Setja greiðsluskilmála fyrir viðskiptavin

[!include[task guide banner](../../includes/task-guide-banner.md)]

Þetta ferli skilgreinir staðgreiðsluafslátt og uppsetning gjalddaga. Þessi leiðarvísi fyrir verk notar sýnigögn USMF fyrirtækis.

1. Fara í Viðskiptakröfur > Uppsetningar greiðslu > Greiðsludagar.
    * Uppsetning Greiðsluskilmála er samnýtt fyrir Viðskiptakröfur og Viðskiptaskuldir. Ef verið er að skilgreina það í kerfinu, hún verður tiltæk í hinu kerfi einnig. Fyrir þessa leiðarvísi fyrir verk, ég að setja upp allar greiðsluskilmála undir viðskiptakröfur.  
2. Smellið á „Nýtt“.
    * Stofna greiðsludag þarfnist skal greiðsluskilmála þínir tiltekinn dag vikunnar (Mánudegi, Þriðjudegi, o. s. frv) eða á tilteknum degi hvers mánaðar (5., 10., o. s. frv).  
3. Í svæðið dagur Greiðslu er að færa inn Kenni fyrir greiðsludaginn í svæðið dagur greiðslu.
4. Færið inn lýsingu á greiðsludegi í svæðinu Lýsing..
5. Í svæðinu Viku/Mánuður velja Viku eða Mánuð.
    * Ef óskað er að færa inn dag vikunnar, eins og Mánudegi, veljið Viku. Ef óskað er að færa inn dagsetningu í mánuði, svo sem 10, veljið Mánuð. Velja Mánuð fyrir þetta dæmi.  
6. Í mánaðardagur svæðinu, færið inn dagsetningu.
    * Ætti að færa inn dagsetninguna sem tölu, til dæmis "10" og ekki sem ‚10.'.  
7. Smellið á „Vista“.
8. Lokið síðunni.
9. Fara í Viðskiptakröfur > Uppsetning greiðslu > Greiðsluskilmálar.
10. Smellið á „Nýtt“.
    * Greiðsluskilmálar er notuð til að skilgreina hvernig gjalddagar verður reiknuð. Uppsetning dagsetning staðgreiðsluafsláttar er skilgreind á sérstakri síðu.  
11. Færið inn Kenni í reitnum greiðsluskilmálar í reitnum greiðsluskilmálar.
12. Færið inn lýsingu í svæðinu Lýsingu.
13. Veljið greiðslumáta eins og Greiðslukröfu, Nettó, Gildandi mánuður, o.s.frv.
    * Greiðsluskilmálar eru notaðir til að skilgreina upphaf fyrir útreikning gjalddaga.  Til dæmis, Nettó er notað ef gjalddagi er alltaf ákveðnum fjölda mánaða eða daga eftir gjalddaga reiknings. Hægt er að nota Greiðslukröfu þegar greiðslu er krafist við reikninginn, svo ekki sé reiknaður út gjalddagi. Veljið Gildandi mánuð fyrir þennan leiðarvísi fyrir verk.  
14. Veljið greiðsludag ef tiltekinn dag, viku eða dagsetningu eru teknar með í útreikningnum.
    * Eftir greiðsluskilmála, má færa inn magn í Mánuðum eða Dögum. Eða hægt er að nota greiðsluáætlun eða greiðsludag til að ' bæta ' við lok greiðsluaðferðar. Gjalddagi verður alltaf að vera 10 næsta mánuð, veljið greiðsludag sem á 10.  
15. Smellið á „Vista“.
16. Lokið síðunni.
17. Fara í Viðskiptakröfur> Greiðsluuppsetning > Staðgreiðsluafsláttur.
18. Smellið á „Nýtt“.
    * Þessi síða er notuð til að skilgreina hvernig dagsetning staðgreiðsluafsláttar reiknaðar.  
19. Færið inn Kenni í svæðinu staðgreiðsluafslátt í svæðinu staðgreiðsluafslátt.
20. Færið inn lýsingu í svæðinu Lýsingu.
21. Ef lagskipt staðgreiðsluafsláttar er tiltækur skal velja Næsta afsláttarkóða sem á við eftir þennan nýja staðgreiðsluafslátt.
22. Færið inn fjölda daga sem er notað til að reikna út dagsetningu staðgreiðsluafsláttar
    * Ef Nettó reglu er valinn er fjöldi daga bætt við dagsetningu reiknings til að reikna út dagsetningu staðgreiðsluafsláttar.  
23. Færið inn prósentutala staðgreiðsluafsláttar.
24. Færið inn aðallykilinn sem staðgreiðsluafsláttur eru bókuð fyrir reikninga viðskiptavina.
25. Veljið valkost í svæðinu Afsláttur mótlykla.
    * Ef valið er ‚Lyklar í línum reiknings' valið staðgreiðsluafsláttur verður bókaður á sama aðallykil eignar/kostnað í línum reiknings lánardrottins. Ef valið er 'Nota aðallykil fyrir reikninga lánardrottins' verður staðgreiðsluafsláttar bókuð í aðallykil sem er skilgreindur á 'aðallykils fyrir reikninga lánardrottins'. Í þessu dæmi, veljið 'Nota aðallykil fyrir reikninga lánardrottins.'  
26. Færið inn aðallykilinn sem staðgreiðsluafsláttur eru bókuð fyrir reikninga lánardrottins.
27. Smellið á „Vista“.


