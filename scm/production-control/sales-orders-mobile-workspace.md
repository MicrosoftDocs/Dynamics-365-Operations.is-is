---
title: "Sölupantanavinnusvæði í farsíma fyrir forritið Microsoft Dynamics 365 for Operations"
description: "Með sölupantanavinnusvæði í farsíma er hægt setja sig inn í sölupantanirnar hvar og hvenær sem er."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 267134
ms.assetid: dbc6dc39-b535-42d3-9fbd-4724597388ad
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mirzaab
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 7a0a2af2094e3e5be757d3dd82255769677b96ea
ms.openlocfilehash: 851c53e1c53fb37488ed86e25e3ede83ca0541db
ms.lasthandoff: 03/31/2017


---

# <a name="sales-orders-mobile-workspace-for-microsoft-dynamics-365-for-operations-app"></a>Sölupantanavinnusvæði í farsíma fyrir forritið Microsoft Dynamics 365 for Operations

Með sölupantanavinnusvæði í farsíma er hægt setja sig inn í sölupantanirnar hvar og hvenær sem er. 

<a name="prerequisites"></a>Forkröfur
-------------

| Skilyrði                                                         | lýsing                                                                                                                                                                   |
|----------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Lesa um Microsoft Dynamics 365 for Operations verkvang | [Microsoft Dynamics 365 for Operations verkvangur](/dynamics365/operations/dev-itpro/mobile-apps/mobile-platform)                                                              |
| Dynamics 365 for Operations                                          | Vertu viss um að þú sért að nota umhverfi sem er með Microsoft Dynamics 365 for Operations útgáfu 1611 og uppfærslu verkvangs Microsoft Dynamics for Operations 3 (nóvember 2016). |
| Bráðabót KB 3215650                                                    | Setja upp bráðabót til að virkja vinnusvæðin sem veitt eru í Microsoft Dynamics 365 for Operations.                                                                       |
| Lýsingarlína fartækis með forritið Dynamics 365 for Operations uppsett | Sækja forritið Dynamics 365 for Operations úr forritaverslun fartækis.                                                                                                      |

## <a name="overview"></a>Yfirlit
Þetta farsímavinnusvæði tengist forritinu Dynamics 365 for Operations og gerir þér kleift að skoða nákvæmar upplýsingar um hverja sölupöntun, svo sem stöðu pöntunar, upplýsingar um viðskiptavin og tengslaupplýsingar þess sem pantar. Farsímavinnusvæðið veitir skjótt yfirlit sölupantana. Hægt er að skoða sölupantanir eftir viðskiptavini, eða skoða allar sölupantanir eða skoða upplýsingar um tiltekna sölupöntun. Farsímavinnusvæði veitir tvö yfirlit til aðstoðar við að greina sölupantanir í dýpt.

### <a name="view-all-sales-orders"></a>Skoða allar sölupantanir

Þetta yfirlit sýnir allar sölupantanir.

-   Notið eina af eftirfarandi síum til að velja sölupantanir sem skoða á.
    -   Leita eftir sölupöntun
    -   Leita eftir viðskiptavinalykli
    -   Leita eftir nafni viðskiptavinar
    -   Leita eftir stöðu
    -   Leita eftir losunarstöðu
    -   Leita eftir stofndagsetningu og -tíma

<!-- -->

-   Eftir að sölupantanir eru valdar er hægt að skoða upplýsingar um ákveðnar pantanir. Einkum er hægt að skoða:
    -   Upplýsingar um nafn og aðsetur viðskiptavinar
    -   Mismunandi dagsetningar sölupantana, svo sem umbeðna sendingardagsetningu og staðfesta sendingardagsetningu
    -   Tengslaupplýsingar þess sem pantar
    -   Tengslaupplýsingar viðskiptavinar
    -   Pantanalínur
    -   Sendingar sem sýna hvernig og hvenær sölupöntun hefur verið send

### <a name="view-orders-for-a-customer-"></a>Skoða pantanir fyrir viðskiptavin** **

Þetta yfirlit sýnir sölupantanir á hvern viðskiptavin

-   Notið eina af eftirfarandi síur til að skoða pantanir fyrir viðskiptavini.
    -   Leita eftir nafni
    -   Leita eftir lykli

<!-- -->

-   Þegar viðskiptavinur hefur verið valinn er hægt að skoða:
    -   Heiti og flokkur viðskiptavinar
    -   Tengslaupplýsingar viðskiptavinar
    -   Sölupantanir viðskiptavina og upplýsingar um sölupantanir:
        -   Upplýsingar um nafn og aðsetur viðskiptavinar
        -   Mismunandi dagsetningar sölupöntunar
        -   Tengslaupplýsingar þess sem pantar
        -   Tengslaupplýsingar viðskiptavinar
        -   Pantanalínur
        -   Sendingar sem sýna hvernig og hvenær sölupöntun hefur verið send

## <a name="get-started"></a>Hefjast handa
Fylgið eftirfarandi skrefum til að hefja notkun á sölupantanavinnusvæði í farsíma í fartæki fyrirtækisins.

1.  Sæktu forritið Dynamics 365 for Operations úr forritaverslun farsímans og settu það upp.
2.  Ræstu forritið í snjallsímanum.
3.  Færðu inn vefslóð þína fyrir Dynamics 365.
4.  Skráðu fyrirtækið sem á að skrá sig inn á . Til dæmis: Færið inn **USMF**.
5.  Fyrsta skipti‘ sem þú skráir þig inn verðurðu beðin um notandanafn og aðgangsorð fyrir þinn Microsoft Dynamics 365 for Operations reikning. Færðu inn skilríki Eftir að þú skrá inn, sérðu tiltækt vinnusvæði fyrir Þitt fyrirtæki.

Til að skoða vinnusvæði í farsímaforritinu verður fyrst að gefa út æskileg vinnusvæði í forritið Dynamics 365 for Operations.

1.  Ræstu Dynamics 365 for Operations.
2.  Opnaðu **Kerfisstjórnun** &gt; **Uppsetning** &gt; **kerfisfæribreytur**.
3.  Veldu **Stjórna fartækjaforriti**.
4.  Velja vinnusvæðið til að birta í verkvangi farsíma.
5.  Veldu **Birta vinnusvæði**.
6.  Endurhlaða Þitt tæki til að sjá útgefin vinnusvæði.

## <a name="view-information-about-sales-orders-for-a-customer"></a>Skoða upplýsingar um sölupantanir fyrir viðskiptavin.
1.  Í farsímanum velurðu vinnusvæðið **Sölupantanir**.
2.  Veldu **Skoða pantanir fyrir viðskiptavin**.
3.  Notið ** Lykil ** eða ** Nafn Viðskiptavinar ** upplýsingar til að finna æskilegan viðskiptavin.
4.  Velja viðskiptavin.
5.  Veldu **Tengslaupplýsingar** eða **Sölupantanir**.
6.  Ef **Sölupantanir** er valið birtist lista yfir sölupantanir fyrir viðskiptavin.
7.  Veldu **Velja sölupöntun**.
8.  Hér geturðu skoðað upplýsingar um sölupöntunarlínur, sendingar, tengslaupplýsingar viðskiptavinar og tengslaupplýsingar þess sem pantar.




