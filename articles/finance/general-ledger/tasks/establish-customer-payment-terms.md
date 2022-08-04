---
title: Setja greiðsluskilmála fyrir viðskiptavin
description: Þetta ferli skilgreinir staðgreiðsluafslátt og uppsetning gjalddaga.
author: aprilolson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: PaymDay, PaymTerm, CashDisc
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6069d28d84ab1705fd62a33cea7e0b923f0e0705
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/29/2022
ms.locfileid: "9065709"
---
# <a name="establish-customer-payment-terms"></a>Setja greiðsluskilmála fyrir viðskiptavin

[!include [banner](../../includes/banner.md)]

Þetta ferli skilgreinir staðgreiðsluafslátt og uppsetning gjalddaga. Þessi leiðarvísi fyrir verk notar sýnigögn USMF fyrirtækis.

1. Farðu í **Skoðunarrúðu > Kerfiseiningar > Viðskiptakröfur > Greiðsluuppsetning > Greiðsludagar**. Uppsetning **Greiðsluskilmála** er samnýtt fyrir **Viðskiptakröfur** og **Viðskiptaskuldir**. Ef verið er að skilgreina það í kerfinu, hún verður tiltæk í hinu kerfi einnig. Fyrir þessa verkefnaleiðbeiningar, allir greiðsluskilmálar skv **Reikningur fáanlegur** eru settar upp.
2. Smellt er á **Nýtt**. Stofna greiðsludag þarfnist skal greiðsluskilmála þínir tiltekinn dag vikunnar (Mánudegi, Þriðjudegi, o. s. frv) eða á tilteknum degi hvers mánaðar (5., 10., o. s. frv). 
3. Færið inn kenni í reitnum **Greiðsludagur**.
4. Færið inn lýsingu á greiðsludegi í reitinn **Lýsing**.
5. Í reitnum **Viku/Mánuður** velurðu Viku eða Mánuð. Ef óskað er að færa inn dag vikunnar, eins og Mánudegi, veljið Viku. Ef óskað er að færa inn dagsetningu í mánuði, svo sem 10, veljið Mánuð. Velja Mánuð fyrir þetta dæmi. 
6. Í reitnum **Mánaðardagur** færið inn dagsetningu. Ætti að færa inn dagsetninguna sem tölu, til dæmis "10" og ekki sem ‚10.'. 
7. Smellt er á **Vista**.
8. Lokið síðunni.
9. Farðu í **Skoðunarrúðu > Kerfiseiningar > Viðskiptakröfur > Greiðsluuppsetning > Greiðsluskilmálar**.
10. Smellt er á **Nýtt**. **Greiðsluskilmálar** er notað til að skilgreina hvernig gjalddagar verða reiknaðir. Uppsetning dagsetning staðgreiðsluafsláttar er skilgreind á sérstakri síðu. 
11. Færið inn kenni í reitnum **Greiðsluskilmálar**.
12. Í reitnum **Lýsing** skal færa inn lýsingu.
13. Veldu a **Greiðslumáti** eins og **COD**, **·**, **mánuður**, osfrv **Greiðslumáti** er notað til að skilgreina upphaf þess hvernig gjaldfallið verður reiknað út. Til dæmis, **Nettó** er notað ef gjalddagi er alltaf ákveðinn fjöldi mánaða eða daga frá reikningsdegi. **COD** hægt að nota þegar greiðslu er krafist á reikningi, þannig að gjalddagi væri ekki reiknaður. Veldu **Núverandi mánuður** fyrir þessa verkefnaleiðbeiningar.  
14. Veljið **greiðsludag** ef tiltekinn dagur, vika eða dagsetning eru tekin með í útreikningnum. Eftir greiðsluskilmála, má færa inn magn í Mánuðum eða Dögum. Eða þú getur notað **Greiðsluáætlun** eða **Greiðsludagur** að 'bæta við' í lokin á **Greiðslumáti**. Gjalddagi verður alltaf að vera 10. næsta mánaðar, veljið **greiðsludag** sem er þann 10. Ef þú ert að nota a **Greiðsludagatal**, er hægt að skilgreina hvernig gjalddagi er ákvarðaður þegar útreiknuð dagsetning lendir á óvirkum degi. Upphaflegur gjalddagi er reiknaður út frá almanaksdögum. Ef útreiknuð dagsetning lendir á óvirkum degi er hægt að breyta reiknuðum gjalddaga annað hvort að næsta virka degi eða fyrri virka degi.
15. Smelltu á **Vista**.
16. Lokið síðunni.
17. Fara í **Viðskiptakröfur> Greiðsluuppsetning > Staðgreiðsluafsláttur**.
18. Smellt er á **Nýtt**. Þessi síða er notuð til að skilgreina hvernig dagsetning staðgreiðsluafsláttar reiknaðar. 
19. Færið inn kenni í reitnum **Staðgreiðsluafsláttur**.
20. Í reitnum **Lýsing** skal færa inn lýsingu.
21. Ef lagskipt staðgreiðsluafsláttar er tiltækur skal velja **Næsta afsláttarkóða** sem á við eftir þennan nýja staðgreiðsluafslátt.
22. Í reitinn **Daga** skal færa inn fjölda daga sem er notað til að reikna út dagsetningu staðgreiðsluafsláttar Ef meginreglan **Nettó** er valin er fjöldi daga bætt við dagsetningu reiknings til að reikna út dagsetningu staðgreiðsluafsláttar.  
23. Í reitinn **Afsláttarprósenta** skal færa inn prósentu staðgreiðsluafsláttar.
24. Í **Aðalreikningur fyrir afslátt viðskiptavina** slærðu inn aðalreikninginn sem staðgreiðsluafsláttur birtir fyrir reikninga viðskiptavina.
25. Veljið valkost í reitnum **Afsláttur mótlykla**. Ef valið er ‚Lyklar í línum reiknings' valið staðgreiðsluafsláttur verður bókaður á sama aðallykil eignar/kostnað í línum reiknings lánardrottins. Ef þú velur **Notaðu aðalreikning fyrir reikninga lánardrottins**, staðgreiðsluafslátturinn mun birtast á aðalreikninginn sem þú skilgreinir í **Aðalreikningur fyrir reikninga lánardrottins**. Fyrir þetta dæmi, veldu **Notaðu aðalreikning fyrir reikninga lánardrottins**. 
26. Í reitnum **Aðalreikningur fyrir afslátt lánardrottna** slærðu inn aðalreikninginn sem staðgreiðsluafsláttur birtir fyrir reikninga lánardrottna.
27. Smellt er á **Vista**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
