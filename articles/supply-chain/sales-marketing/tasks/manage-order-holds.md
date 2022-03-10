---
title: Stjórna pöntunum í bið
description: Þetta ferli sýnir hvernig setja sölupantanir viðskiptavina í bið, hvernig vinna með biðstöðu greiðsluferlis og hvernig fjarlægja bið af pöntun.
author: Henrikan
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: MCRHoldCodeTable, SalesTableListPage, SalesCreateOrder, SalesTable, MCRHoldCodeTrans, MCRHoldCheckOutOverride, MCRHoldCodeTable, MCRItemListCopying, MCRItemListTable, MCROMHoldList
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 938b21b66b7b61452be104936877278a3bc120f2
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 09/29/2021
ms.locfileid: "7566293"
---
# <a name="manage-order-holds"></a>Stjórna pöntunum í bið

[!include [banner](../../includes/banner.md)]

Þetta ferli sýnir hvernig setja sölupantanir viðskiptavina í bið, hvernig vinna með biðstöðu greiðsluferlis og hvernig fjarlægja bið af pöntun. Pöntun kann að vera sett í bið af ýmsum ástæðum. Til dæmis gætirðu verið með pöntun í bið þar til hægt er að staðfesta aðsetur viðskiptavinar eða greiðsluhætti eða þar til stjórnandinn getur farið yfir lánamark viðskiptavinar. Þegar pöntun er í bið er ekki hægt að vinna af vörugeymslu til afhendingar. 

Hægt er að keyra þessa ferli í sýnifyrirtækinu USMF eða í eigin gögnum.


## <a name="set-up-order-holds"></a>Setja upp biðstöðu pöntunar
1. Farðu í **Skoðunarrúðu > Kerfiseiningar > Sala og markaðssetning > Uppsetning > Sölupantanir > Biðkóðar pantana**.
2. Smellt er á **Nýtt**.
3. Í reitinn **Biðkóði** skal færa inn gildi. Til dæmis, skrifið Kalla aftur.  
4. Í reitinn **Lýsing** skal slá inn gildi.
    - Til dæmis, Pöntun haldið í bið eftir símtal frá viðskiptavinur.  
    - Annars er hægt að velja gátreitinn **Fjarlægja frátekningu** til að fjarlægja allar efnislegur frátekning úr pöntun þegar biðkóði er bætti við.  
5. Smellt er á **Vista**.

## <a name="place-order-on-hold"></a>Setja pöntun í bið
1. Farðu í **Skoðunarrúðu > Kerfiseiningar > Sala og markaðssetning > Sölupantanir > Allar sölupantanir**.
2. Smellt er á **Nýtt**.
3. Í reitnum **Viðskiptavinalykill** skal færa inn eða velja gildi.
4. Smellt er á **OK**.
5. Í reitinn **Vörunúmer** skal slá inn eða velja gildi.
6. Í reitnum **Magn** slærðu inn tölu.
7. Á **Aðgerðasvæðinu** skal smellt á **Sölupöntun**.
8. Smellt er á **Biðstöður pantana**.
9. Smellt er á **Nýtt**.
10. Í svæði **Biðkóði** skal velja kóða sem stofnaður í fyrra undirverk.
11. Smellt er á **Vista**.
12. Lokið síðunni.
13. Farðu í **Sölu og markaðssetningu > sölupöntun > Allar sölupantanir**.
14. Í listanum skal merkja valda línu. Pantanir sem núna í bið eru með merkt svæði „Ekki keyra“ og „Í biðstöðu“.
15. Á aðgerðasvæðinu er smellt á **Taka til og pakka**.

## <a name="manage-order-holds"></a>Stjórna pöntunum í bið
1. Farðu í **Sala og markaðssetning > Sölupöntun > Opnar pantanir > Pantanir í bið**. Síðan **Pantanir í bið** virkar sem vinnubekkur þar sem fá yfirlit yfir allar núgildandi og unnar biðstöður, vinna með þær og tengdar sölupantanir.     
2. Í listanum skal merkja valda línu.
3. Á **aðgerðarúðunni** skal smella á **Setja greiðsluferli í bið**.
4. Smella skal á **Greiðsluferli**.
5. Í listanum skal afmerkja valda línu. Reiturinn **Greiðsluferli** birtir núna notandakenni þitt.   
6. Smelltu á **Hreinsa greiðsluferli**.
7. Í **aðgerðaglugganum** smellirðu á **Hreinsa biðstöðu**.
    - Þegar þú tilbúið að fjarlægja í bið og leyfa pöntun halda áfram í næsta útskráningarskref verður að hreinsa í bið. Ef ekki þarf að breyta pöntun má keyra aðgerð Hreinsa bið. Þegar bið er hreinsa er hægt að nota aðgerð Hreinsa og breyta ef uppfæra þarf pöntun.      
    - Aðgerðin **Hreinsa og senda** á aðeins við þegar aðgerðin Símaver er notað.  
8. Smelltu á **Hreinsa biðstöðu**. Biðstaða hefur verið fjarlægja af pöntun og fjarlægt af lista yfir virkar biðstöður. Til að sjá allar biðstöður eða hlutmengi þeirra samkvæmt tiltekinni stöðu skal breyta gildi í svæði Sýna.     



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]