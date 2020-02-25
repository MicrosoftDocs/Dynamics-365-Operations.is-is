---
title: Útboðsbundin afsláttur
description: Þetta efni veitir yfirlit yfir virkni sem við skulum láta smásala stilla afslátt fyrir ákveðnar útboðsgerðir.
author: bebeale
manager: AnnBe
ms.date: 10/30/19
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailTenderDiscount
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: shajain
ms.search.validFrom: 2018-10-31
ms.dyn365.ops.version: Version 10.0.7
ms.openlocfilehash: 06de834d8081056fab6f628b24ec3eb1cb43d6f6
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/01/2020
ms.locfileid: "3022882"
---
# <a name="tender-based-discounts"></a>Útboðsbundin afsláttur

[!include [banner](includes/banner.md)]


Það er algengt hjá smásöluaðilum að gefa út einkakennd kreditkort. Söluaðilarnir njóta góðs af því að þeir fá valinn vexti frá bönkunum. Þar að auki, vegna þess að þessi kreditkort geta hvatt viðskiptavini til að heimsækja verslunina oftar, hjálpa þau til við að bæta niðurstöðulínu verslunarinnar. Þess vegna hafa smásalar hvata til að auka notkun viðskiptavina á vörumerkjakreditkortunum sínum. Til að ná þessu markmiði veita þeir oft frekari afslátt til viðskiptavina sem nota þessi kreditkort.

Að öðrum kosti gætu smásalar sem ekki bjóða upp á vörumerkt kreditkort viljað hvetja viðskiptavini til að greiða með því að nota aðrar útboðsgerðir, svo sem reiðufé, gjafakort eða vildarpunkta. Með þessum hætti geta þeir hjálpað til við að draga úr kostnaði við afgreiðslugjöld kreditkorta. Þess vegna gætu smásalar veitt afslátt til viðskiptavina sem nota þessar aðrar útboðsgerðir.

Í Microsoft Dynamics 365 Commerce geta smásalar stillt afsláttarprósentu sem er beitt á hæfar línur ef viðskiptavinurinn borgar með því að nota valda útboðsgerð. Viðskiptavinurinn getur ákveðið hvort hann greiði hlutagreiðslu eða fulla greiðslu og Commerce ákvarðar viðeigandi afsláttarfjárhæð. Athugaðu að afslátturinn er alltaf gefinn á upphæð fyrir skatta hæfra hlutanna.

Útboðsbundin afsláttur keppir ekki við vöruafslátt, eins og reglubundinn eða handvirkan afslátt. Þeir eru alltaf samsettir á vöruafslætti. Þess vegna, jafnvel þótt beinn reglubundinn afsláttur sé notaður á vöru, er útboðsbundnum afslætti ennþá beitt ofan á beinan reglubundinn afslátt. Sömuleiðis, ef þröskuldarafslætti er beitt á færsluna og útboðsbundinn afsláttur lækkar samtöluna undir viðmiðunarmörk, er þröskuldafslætti enn beitt á færsluna.

Jafnvel þó að útboðsbyggður afsláttur dragi úr millisamtölu færslunnar hefur það ekki áhrif á sjálfvirk gjöld sem er beitt á færsluna. Til dæmis, ef afhendingargjöld eru reiknuð sem $5 vegna þess að millisamtalan var yfir $100, og útboðsbundinn afsláttur minnkar magnið þannig að það er minna en $100, eru afhendingargjöldin ennþá $5 fyrir pöntunina.


> [!NOTE]
> Útboðsbundnum afslætti er hlutfallslega dreift til hæfra sölulína og lækkar upphæð fyrir skatta af einstökum línum. Ef margfeldi útboðsafsláttar er stillt fyrir útboðsgerð (til dæmis reiðufé) er aðeins besti útboðsbundna afslættinum beitt.

Útboðsbundnum afslætti er aðeins hægt að beita á sölulínur þar sem verðið er ekki læst. Ef nýjum sölulínum er bætt við pöntun er útboðsbundnum afslætti aðeins beitt á nýju sölulínurnar meðan á greiðslu stendur. Þegar pöntun viðskiptavinar um afhendingu eða sendingu er sett er útboðsbundnum afslætti aðeins beitt á upphæð innborgunar. Eftir að pöntunin hefur verið gerð, meðan á uppfyllingu stendur, eru verð á sölulínunum læst. Þess vegna er engum útboðsbundnum afslætti beitt á neina stöðu sem er greidd við afhendingu eða heimiluð meðan á sendingu stendur. Útboðsbundnum afslætti er aðeins hægt að beita á alla upphæð viðskiptavinapöntunar ef smásalinn innheimtir alla upphæðina sem innborgun meðan pöntunin er gerð.

> [!IMPORTANT]
> Í Commerce eru afslættir sem byggjast á útboði takmarkaðir við tvær greiðslur: kreditkort og reiðufé.

## <a name="pos-user-experience"></a>Notandareynsla POS

Ef útboðsbundinn afsláttur er settur upp fyrir reiðufé og gjaldkeri á sölustaðnum (POS) velur hnapp sem er kortlagður við Pay cash-aðgerðina, er útboðsbundinn afsláttur sjálfkrafa beittur við viðskiptin. Minni upphæðin er síðan sýnd sem staða. Hins vegar, ef gjaldkerinn velur hnappinn **Til baka** á greiðsluskjánum er afslátturinn fjarlægður og upphafleg upphæð er sýnd á viðskiptaskjánum. Útboðsbundinn afsláttur er fjarlægður ef greiðslulínan er ógild.

Við kortagreiðslur geta smásalar stillt útboðsbundinn afslátt á einni eða fleiri tegundum kreditkorta. Hins vegar getur kerfið ekki staðfest þá tegund kreditkorta sem er notuð nema kortið sé heimilað. Ef afslátturinn er notaður eftir heimild verður greiðsluheimildin fyrir stærri upphæð en greiðsluöflunin er fyrir minni upphæð.

Til að koma í veg fyrir þetta ástand, ef viðskiptavinur borgar með kreditkorti, sér gjaldkerinn valmynd sem sýnir kreditkort sem munu veita viðskiptavininum viðbótarsparnað. Gjaldkeri getur síðan spurt hvort viðskiptavinurinn vilji nota eitt af völdu kortunum til að fá viðbótarafslátt. Ef gjaldkerinn notar valið kort er útboðsbundnum afslætti beitt á færsluna og lækkuð upphæð er sýnd á greiðsluskjánum. Heimildin verður fyrir lægri fjárhæð. Ef viðskiptavinurinn setur inn kort sem er frábrugðið kortinu sem gjaldkerinn valdi, birtast villuboð og heimildin fellur úr gildi.


## <a name="call-center-user-experience"></a>Reynsla af símaþjónustuverum

Þegar notandinn velur **Lokið** meðan á pöntun miðstöðvar stendur er skjárinn **Heildartölur** sýndur. Til að byrja með eru heildartölurnar á þessum skjá ekki með afslætti sem byggir á útboðum því greiðslumátinn hefur ekki enn verið valinn. Á skjánum **Bæta við greiðslu**, ef notandinn velur greiðslumáta sem útboðsbundinn afsláttur er stilltur fyrir, er greiðslufjárhæðin sjálfkrafa leiðrétt þannig að hún endurspeglar upphæð með afslætti. Eins og viðskiptavinurinn í POS, getur viðskiptavinur símaþjónustunnar ákveðið hvort greiða eigi alla greiðsluna eða að hluta til. Miðað við fjárhæðina sem er greidd er útboðsbundnum afslætti beitt á sölupöntunina.

> [!NOTE]
> Staðfesting korta er ekki gerð fyrir pantanir í símaþjónustuver. Til dæmis, ef notandi símaþjónustunnar velur Visa sem kreditkort, en viðskiptavinurinn notar Mastercard, beitir kerfið afslættinum samt sem áður.

## <a name="exclude-items-from-discounts"></a>Útiloka vörur frá afslætti

Söluaðilar velja oft að útiloka sumar vörur, svo sem nýja hluti eða eftirspurn, frá afslætti. Samt sem áður gætu þeir viljað beita afslætti sem byggir á útboðum. Til dæmis, smásali stillir Commerce þannig að hún leyfir ekki vöruafslátt eða handvirkan afslátt. Hins vegar, ef viðskiptavinurinn greiðir með því að nota valið útboð, beitir Commerce útboðsbundnum afslætti samt sem áður. Til að setja upp Commerce með þessum hætti verða smásalar að fara í **Vöruupplýsingastjórnun > Afurðir > Útgefnar afurðir**, velja vöruna og síðan, á flýtiflipanum **Commerce**, stilla valkostina **Koma í veg fyrir alla afslætti** og **Koma í veg fyrir útboð á grundvelli útboða** á **Nei** og valkostina **Koma í veg fyrir smásöluafslátt** og **Koma í veg fyrir handvirka afslætti** á **Já**.

> [!NOTE]
> Þegar skilgreiningin **Koma í veg fyrir allan afslátt** er stillt á **Já** verður engum afslætti beitt á vöruna. Ekki einu sinni útboðsbundnum afslætti verður beitt.
