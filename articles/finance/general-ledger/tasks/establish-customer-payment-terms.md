---
title: Setja greiðsluskilmála fyrir viðskiptavin
description: Þetta ferli skilgreinir staðgreiðsluafslátt og uppsetning gjalddaga.
author: aprilolson
ms.date: 08/29/2022
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
ms.openlocfilehash: 9b2ae5e63a2efb4bc913efa4d88c65a70133a2d9
ms.sourcegitcommit: f96e5dec5a808d9819d2a23b8e15ce00aeff475b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/10/2022
ms.locfileid: "9752777"
---
# <a name="establish-customer-payment-terms"></a>Setja greiðsluskilmála fyrir viðskiptavin

[!include [banner](../../includes/banner.md)]

Þetta ferli skilgreinir staðgreiðsluafslátt og uppsetning gjalddaga. Þessi leiðarvísi fyrir verk notar sýnigögn USMF fyrirtækis.

1. Farðu í **Skoðunarrúðu > Kerfiseiningar > Viðskiptakröfur > Greiðsluuppsetning > Greiðsludagar**. Uppsetning **Greiðsluskilmála** er samnýtt fyrir **Viðskiptakröfur** og **Viðskiptaskuldir**. Ef verið er að skilgreina það í kerfinu, hún verður tiltæk í hinu kerfi einnig. Fyrir þessa leiðarvísi fyrir verk, eru allir greiðsluskilmálar undir **Viðskiptakröfur** settir upp.
2. Smellt er á **Nýtt**. Stofna greiðsludag þarfnist skal greiðsluskilmála þínir tiltekinn dag vikunnar (Mánudegi, Þriðjudegi, o. s. frv) eða á tilteknum degi hvers mánaðar (5., 10., o. s. frv). 
3. Færið inn kenni í reitnum **Greiðsludagur**.
4. Færið inn lýsingu á greiðsludegi í reitinn **Lýsing**.
5. Í reitnum **Viku/Mánuður** velurðu Viku eða Mánuð. Ef óskað er að færa inn dag vikunnar, eins og Mánudegi, veljið Viku. Ef óskað er að færa inn dagsetningu í mánuði, svo sem 10, veljið Mánuð. Velja Mánuð fyrir þetta dæmi. 
6. Í reitnum **Mánaðardagur** færið inn dagsetningu. Ætti að færa inn dagsetninguna sem tölu, til dæmis "10" og ekki sem ‚10.'. 
7. Smellt er á **Vista**.
8. Lokið síðunni.
9. Farðu í **Skoðunarrúðu > Kerfiseiningar > Viðskiptakröfur > Greiðsluuppsetning > Greiðsluskilmálar**. 

>[!NOTE] 
>Ef **Greiðsluskilmálar** eru **Reiðufél** verður reiturinn **Greiðsla í reiðufé** á síðunni **Greiðsluskilmálar** að vera **Nei**.

10. Smellt er á **Nýtt**. **Greiðsluskilmálar** er notuð til að skilgreina hvernig gjalddagar verður reiknuð. Uppsetning dagsetning staðgreiðsluafsláttar er skilgreind á sérstakri síðu. 
11. Færið inn kenni í reitnum **Greiðsluskilmálar**.
12. Í reitnum **Lýsing** skal færa inn lýsingu.
13. Veljið **Greiðslumáti** á borði við **Greiðslukrafa**, **Nettó**, **Núverandi mánuður**, o.s.frv. **Greiðslumáti** er notaður til að skilgreina upphaf fyrir útreikning gjalddaga. Til dæmis er **Nettó** notað ef gjalddagi er alltaf ákveðnum fjölda mánuða eða daga eftir gjalddaga reiknings. Hægt er að nota **Greiðslukröf** u þegar greiðslu er krafist við reikninginn, svo ekki sé reiknaður út gjalddagi. Veljið **Núverandi mánuður** fyrir þennan leiðarvísi fyrir verk.  
14. Veljið **greiðsludag** ef tiltekinn dagur, vika eða dagsetning eru tekin með í útreikningnum. Eftir greiðsluskilmála, má færa inn magn í Mánuðum eða Dögum. Eða hægt er að nota **greiðsluáætlun** eða **greiðsludag** til að ' bæta ' við lok **greiðsluaðferðar**. Gjalddagi verður alltaf að vera 10. næsta mánaðar, veljið **greiðsludag** sem er þann 10. Ef þú ert að nota **Greiðsludagatal** er hægt að skilgreina hvernig gjalddagi er ákvarðaður þegar útreiknaður dagur lendir á öðrum degi en virkum degi. Upphaflegur skiladagur er reiknaður með almanaksdögum. Ef útreiknaður dagur lendir á öðrum degi en vinnudegi er hægt að leiðrétta útreiknaðan gjalddaga á næsta virka dag eða fyrr.
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
25. Veljið valkost í reitnum **Afsláttur mótlykla**. Ef valið er ‚Lyklar í línum reiknings' valið staðgreiðsluafsláttur verður bókaður á sama aðallykil eignar/kostnað í línum reiknings lánardrottins. Ef valið er **Nota aðallykil fyrir reikninga lánardrottins** verður staðgreiðsluafsláttar bókuð í aðallykil sem er skilgreindur á **Aðallykill fyrir reikninga lánardrottins**. Í þessu dæmi, veljið **Nota aðallykil fyrir reikninga lánardrottins**. 
26. Í reitnum **Aðalreikningur fyrir afslátt lánardrottna** slærðu inn aðalreikninginn sem staðgreiðsluafsláttur birtir fyrir reikninga lánardrottna.
27. Smellt er á **Vista**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
