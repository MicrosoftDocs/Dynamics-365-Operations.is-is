---
title: "Sölupantanir fartæki vinnusvæði fyrir Microsoft Dynamics 365 fyrir Aðgerðir forrits"
description: "Með sölupantanir fartæki vinnusvæðið, er hægt setja sig inn í sölupantanirnar hvar og anytime."
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

# <a name="sales-orders-mobile-workspace-for-microsoft-dynamics-365-for-operations-app"></a>Sölupantanir fartæki vinnusvæði fyrir Microsoft Dynamics 365 fyrir Aðgerðir forrits

Með sölupantanir fartæki vinnusvæðið, er hægt setja sig inn í sölupantanirnar hvar og anytime. 

<a name="prerequisites"></a>Forkröfur
-------------

| Skilyrði                                                         | lýsing                                                                                                                                                                   |
|----------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Lesa um Microsoft Dynamics 365 fyrir fartæki svæðis Aðgerðir | [Dynamics 365 fyrir fartæki svæðis Aðgerðir](/dynamics365/operations/dev-itpro/mobile-apps/mobile-platform)                                                              |
| Dynamics 365 fyrir Aðgerðir                                          | Verið viss um að afskriftareglur eru umhverfi sem er með Microsoft Dynamics 365 Aðgerðir útgáfu 1611 og uppfærslu Microsoft Dynamics fyrir Aðgerðir svæðis (Nóvember 2016) 3. |
| Bráðabót KB 3215650                                                    | Setja upp bráðabót til að virkja skal vinnusvæðin sem eru gefnir í Microsoft Dynamics 365 fyrir Aðgerðir.                                                                       |
| Lýsingarlína fartækis með Dynamics 365 fyrir Aðgerðir forrits uppsett | Sækja Dynamics 365 fyrir Aðgerðir forrits úr verslunin fartæki forrits.                                                                                                      |

## <a name="overview"></a>Yfirlit
Þessi fartæki vinnusvæði tengist Dynamics 365 fyrir Aðgerðir forrits og gerir þér kleift að skoða nákvæmar upplýsingar um hverja sölupöntun, svo stöðu pöntunar, upplýsingar um viðskiptavin og tengslaupplýsingar taker pöntun. Fartæki vinnusvæði veitir snatri yfirlit sölupantana. Hægt er að skoða sölupantanir eftir viðskiptavini, eða skoða allar sölupantanir eða skoða upplýsingar um tiltekna sölupöntun. Fartæki vinnusvæði veitir tvö yfirlit til aðstoðar við að greina sölupantanir í dýpt.

### <a name="view-all-sales-orders"></a>Skoða allar sölupantanir

Þetta yfirlit sýnir allar sölupantanir.

-   Notið eina af eftirfarandi síur til að velja sölupantanir sem skoða á.
    -   Leita eftir sölupöntun
    -   Leita eftir viðskiptavinalykil
    -   Leita að nafni viðskiptavinar
    -   Leita eftir stöðu
    -   Leita eftir losunarstaða
    -   Leita eftir tími og dagsetning stofnunar

<!-- -->

-   Eftir að sölupantanir er hægt að skoða upplýsingar um ákveðnar pantanir. Sérstaklega er hægt að skoða:
    -   Nafn og aðsetur upplýsingar viðskiptavinar
    -   Mismunandi sölupöntun dagsetningar, svo sem umbeðin sendingardagsetning og staðfest sendingardagsetning
    -   Tengslaupplýsingar taker pöntun
    -   Tengslaupplýsingar viðskiptavinar
    -   Pantanalínur
    -   Sendingar sem sýna hvernig og hvenær sölupöntun hefur verið send

### <a name="view-orders-for-a-customer-"></a>Skoða pantanir fyrir viðskiptavini ** **

Þetta yfirlit sýnir sölupantanir fyrir hvern viðskiptavin.

-   Notið eina af eftirfarandi síur til að skoða sölupantanir fyrir viðskiptavini.
    -   Leita að nafni
    -   Leita eftir lykli

<!-- -->

-   Eftir að velja viðskiptavin, er hægt að skoða:
    -   Nafn viðskiptavinar og flokk
    -   Tengslaupplýsingar viðskiptavinar
    -   Sölupantanir fyrir viðskiptavini og upplýsingar um sölupantanir:
        -   Nafn og aðsetur upplýsingar viðskiptavinar
        -   Dagsetningar mismunandi sölupöntun
        -   Tengslaupplýsingar taker pöntun
        -   Tengslaupplýsingar viðskiptavinar
        -   Pantanalínur
        -   Sendingar sem sýna hvernig og hvenær sölupöntun hefur verið send

## <a name="get-started"></a>Hefjast handa
Fylgið eftirfarandi skrefum til að byrja með fartæki vinnusvæði sölupantanir í fartæki fyrirtækisins.

1.  Verslunin fartæki forritið á að sækja og setja upp Microsoft Dynamics 365 fyrir Aðgerðir forrits.
2.  Byrja forritið þitt tækis.
3.  Færið inn Vefslóð skal Dynamics 365.
4.  Færið inn fyrirtæki að skrá sig inn á. Til dæmis inn **USMF**.
5.  Í fyrsta sinn sem þú skráir þig inn, verið beðið um notandanafn og aðgangsorð fyrir notanda Microsoft Dynamics 365 fyrir Aðgerðir. Færið inn skilríkjum þínum. Eftir að skrá er að sjá tiltækar vinnusvæða fyrirtækisins.

Til að skoða vinnusvæða fartæki forritið, er verður fyrst að birta skal vinnusvæðin sem óskað er eftir að Dynamics 365 fyrir Aðgerðir forrits.

1.  Ræsa Dynamics 365 aðgerða.
2.  Fara í **kerfisstjórnun**&gt;**Uppsetningu**&gt;**kerfisfæribreytum**.
3.  Veljið **Stjórna fartæki forrits**.
4.  Veljið vinnusvæði til að birta í fartæki svæðis.
5.  Velja **Birta vinnusvæði**.
6.  Endurnýja skal tæki til að sjá birt vinnusvæði.

## <a name="view-information-about-sales-orders-for-a-customer"></a>Skoða upplýsingar um sölupantanir fyrir viðskiptavini
1.  Fartækis, veljið þá **sölupantanir** vinnusvæði.
2.  Velja **Skoða sölupantanir fyrir viðskiptavini**.
3.  Notið ** Lykil ** eða ** Nafn Viðskiptavinar ** upplýsingar til að finna æskilegt viðskiptavinar.
4.  Velja viðskiptavin.
5.  Velja **Tengslaupplýsingar** eða **sölupantanir**.
6.  Ef **sölupantanir** er valinn, lista yfir sölupantanir fyrir viðskiptavini birtist.
7.  Velja **sölupöntun**.
8.  Hér er hægt að skoða upplýsingar um sölupöntunarlínur sendingar, upplýsingar um viðskiptavin og tengslaupplýsingar taker pöntun.




