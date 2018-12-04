--- 
title: "Stjórna pöntunum í bið"
description: "Þetta ferli sýnir hvernig setja sölupantanir viðskiptavina í bið, hvernig vinna með biðstöðu greiðsluferlis og hvernig fjarlægja bið af pöntun."
author: omulvad
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: MCRHoldCodeTable, SalesTableListPage, SalesCreateOrder, SalesTable, MCRHoldCodeTrans
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 3edb8d2fe0fda6634bc2edb8e3bafc5a60344b7a
ms.contentlocale: is-is
ms.lasthandoff: 09/29/2017

---
# <a name="manage-order-holds"></a>Stjórna pöntunum í bið

[!include [task guide banner](../../includes/task-guide-banner.md)]

Þetta ferli sýnir hvernig setja sölupantanir viðskiptavina í bið, hvernig vinna með biðstöðu greiðsluferlis og hvernig fjarlægja bið af pöntun. Pöntun kann að vera sett í bið af ýmsum ástæðum. Til dæmis gætirðu verið með pöntun í bið þar til hægt er að staðfesta aðsetur  viðskiptavinar eða greiðsluhætti eða þar til stjórnandinn getur farið yfir lánamark viðskiptavinar. Þegar pöntun er í bið er ekki hægt að vinna af vörugeymslu til afhendingar. 

Hægt er að keyra þessa ferli í sýnifyrirtækinu USMF eða í eigin gögnum.


## <a name="set-up-order-holds"></a>Setja upp biðstöðu pöntunar
1. Fara í Sala og markaðssetning > Uppsetning > Sölupantanir > Biðkóðar pantana.
2. Smellið á „Nýtt“.
3. Í svæði Biðkóði skal færa inn gildi.
    * Til dæmis, skrifið Hringja aftur.  
4. Sláið inn gildi í reitnum „Lýsing“.
    * Til dæmis, Pöntun haldið í bið eftir símtal frá viðskiptavinur.  
    * Annars er hægt að velja gátreitur Fjarlægja frátekningu til að fjarlægja allar efnislegur frátekning úr pöntun þegar biðkóði er bætti við.  
5. Smellið á „Vista“.

## <a name="place-order-on-hold"></a>Setja pöntun í bið
1. Fara í Sölu og markaðssetningu > sölupöntun > Allar sölupantanir
2. Smellið á „Nýtt“.
3. Færa inn eða veljið gildi í svæðinu Reikningur viðskiptavinar.
4. Smellt er á Í lagi.
5. Í reitinn Vörunúmer skal slá inn eða veldu gildi.
6. Færið inn númer í reitnum „Magn“.
7. Smellið á „Sölupöntun“ á aðgerðarúðunni.
8. Smellt er á Biðstöður pantana.
9. Smellið á „Nýtt“.
10. Í svæði Biðkóði skal velja kóða sem stofnaður í fyrra undirverk.
11. Smellið á „Vista“.
12. Lokið síðunni.
13. Fara í Sölu og markaðssetningu > sölupöntun > Allar sölupantanir
14. Í listanum skal merkja valda línu.
    * Pantanir sem núna í bið eru með merkt svæði „Ekki keyra“ og „Í biðstöðu“.    
15. Smellið á „Tiltekt og pökkun“ á aðgerðarúðunni.

## <a name="manage-order-holds"></a>Stjórna pöntunum í bið
1. Fara í Sala og markaðssetning > Sölupöntun > Opnar pantanir > Pantanir í bið.
    * Síðan Pantanir í bið virkar sem vinnubekkur þar sem fá yfirlit yfir allar núgildandi og unnar biðstöður, vinna með þær og tengdar sölupantanir.      
2. Í listanum skal merkja valda línu.
3. Á aðgerðarúða skal smella á Setja greiðsluferli í bið.
4. Smella skal á Greiðsluferli.
5. Í listanum skal afmerkja valda línu.
    * Svæði Greiðsluferli í birtir núna notandakenni þitt.   
6. Smella á Hreinsa greiðsluferli.
7. Í að smella á Hreinsa biðstöðu.
    * Þegar þú tilbúið að fjarlægja í bið og leyfa pöntun halda áfram í næsta útskráningarskref verður að hreinsa í bið. Ef ekki þarf að breyta pöntun má keyra aðgerð Hreinsa bið. Þegar bið er hreinsa er hægt að nota aðgerð Hreinsa og breyta ef uppfæra þarf pöntun.      
    * Aðgerðin Hreinsa og senda á aðeins við þegar aðgerðin Símaver er notað.  
8. Smella á Hreinsa biðstöðu.
    * Biðstaða hefur verið fjarlægja af pöntun og fjarlægt af lista yfir virkar biðstöður. Til að sjá allar biðstöður eða hlutmengi þeirra samkvæmt tiltekinni stöðu skal breyta gildi í svæði Sýna.     


