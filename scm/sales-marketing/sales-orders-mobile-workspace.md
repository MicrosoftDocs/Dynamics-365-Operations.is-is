---
title: "Fartækjavinnusvæði sölupantana"
description: "Þetta efnisatriði veitir upplýsingar um fartækjavinnusvæði sölupantana, sem er tiltækt fyrir Microsoft Dynamics 365 fyrir Operations farsímaforritið. Þetta vinnusvæði hjálpar þér að hafa yfirsýn yfir sölupantanir þínar hvar og hvenær sem er."
author: YuyuScheller
manager: AnnBe
ms.date: 05/10/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: annbe
ms.search.scope: Operations, Core
ms.custom: 267134
ms.assetid: 0ce96511-002b-4de7-b31e-4303f94edc84
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mirzaab
ms.dyn365.ops.intro: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 11898146a13756a6bb22a769e37e8773484e0d04
ms.contentlocale: is-is
ms.lasthandoff: 05/25/2017


---

# <a name="sales-orders-mobile-workspace"></a>Fartækjavinnusvæði sölupantana

[!include[banner](../includes/banner.md)]


Þetta efnisatriði veitir upplýsingar um fartækjavinnusvæði sölupantana, sem er tiltækt fyrir Microsoft Dynamics 365 fyrir Operations farsímaforritið. Þetta vinnusvæði hjálpar þér að hafa yfirsýn yfir sölupantanir þínar hvar og hvenær sem er. 

<a name="overview-of-the-sales-orders-mobile-workspace"></a>Yfirlit yfir fartækjavinnusvæði sölupantana
---------------------------------------------

Fartækjavinnusvæðið **Sölupantanir** tengist Microsoft Dynamics 365 for Operations og gerir þér kleift að skoða nákvæmar upplýsingar um hverja sölupöntun. Þessar upplýsingar innihalda einnig stöðu pöntunar, upplýsingar fyrir viðskiptavininn og samskiptaupplýsingar fyrir þann sem pantar. Farsímavinnusvæðið **Sölupantanir** veitir fljótlegt yfirlit sölupantana. Hægt er að skoða allar sölupantanir, sölupantanir eftir viðskiptavini, eða skoða upplýsingar um tiltekna sölupöntun. 

Farsímavinnusvæði veitir tvö yfirlit til aðstoðar við að greina sölupantanir í dýpt.

### <a name="view-all-sales-orders"></a>Skoða allar sölupantanir

Þetta yfirlit sýnir allar sölupantanir.

-   Notið eina af eftirfarandi síum til að velja sölupantanir sem skoða á:
    -   Leita eftir sölupöntun
    -   Leita eftir viðskiptavinalykli
    -   Leita eftir nafni viðskiptavinar
    -   Leita eftir stöðu
    -   Leita eftir losunarstöðu
    -   Leita eftir stofndagsetningu og -tíma
    
-   Eftir að sölupantanir eru valdar er hægt að skoða upplýsingar um ákveðnar pantanir. Sérstaklega er hægt að skoða eftirfarandi upplýsingar:
    -   Upplýsingar um nafn og aðsetur viðskiptavinar
    -   Mismunandi dagsetningar fyrir sölupöntun, svo sem umbeðin sendingardagsetning og staðfest sendingardagsetning
    -   Samskiptaupplýsingar fyrir þann sem pantar
    -   Tengslaupplýsingar viðskiptavinar
    -   Pantanalínur
    -   Sendingar sem sýna hvar og hvenær sölupöntun hefur verið send

### <a name="view-orders-for-a-customer"></a>Skoða pantanir fyrir viðskiptavin

Þetta yfirlit sýnir sölupantanir eftir viðskiptavini.

-   Notið eina af eftirfarandi síum til að skoða pantanir fyrir viðskiptavin:
    -   Leita eftir nafni
    -   Leita eftir lykli

-   Þegar viðskiptavinur er valinn er hægt að skoða eftirfarandi upplýsingar:
    -   Heiti og flokkur viðskiptavinar
    -   Tengslaupplýsingar viðskiptavinar
    -   Sölupantanir viðskiptavinar og upplýsingar um sölupantanirnar:
        -   Upplýsingar um nafn og aðsetur viðskiptavinar
        -   Mismunandi dagsetningar sölupöntunar
        -   Samskiptaupplýsingar fyrir þann sem pantar
        -   Tengslaupplýsingar viðskiptavinar
        -   Pantanalínur
        -   Sendingar sem sýna hvar og hvenær sölupöntun hefur verið send

## <a name="prerequisites"></a>Frumskilyrði
Áður en hægt er að nota í fartækjavinnusvæðið **Sölupantanir** skal ganga úr skugga um að kerfisstjórinn hafi stillt eftirfarandi forsendur.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>Skilyrði</th>
<th>Hlutverk</th>
<th>lýsing</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Verður að innleiða Microsoft Dynamics 365 útgáfu 1611 með svæðis uppfærslu 3 eða síðar.</td>
<td>Kerfisstjóri</td>
<td>Ef ekki er þegar Dynamics 365 for Operations starfrækt í fyrirtækinu, skal kerfisstjóri sjá <a href="/dynamics365/operations/dev-itpro/deployment/deploy-demo-environment/">Deploy Microsoft Dynamics 365 fyrir Operations sýnigögn prófunarumhverfi</a>.</td>
</tr>
<tr class="even">
<td>KB 4013633 verður að vera innleitt.</td>
<td>Kerfisstjóri</td>
<td>KB 4013633 (X++ uppfærsla eða lýsigögn bráðabót) inniheldur fjögur fartækjavinnusvæði fyrir afgangakeðju stjórnun. Til að setja upp KB 4013633 verður kerfisstjóri að fylgja eftirfarandi skrefum:
<ol>
<li>Sækja KB 4013633 af Microsoft Dynamics Lifecycle Services (LCS).</li>
<li><a href="/dynamics365/operations/dev-itpro/migration-upgrade/install-metadata-hotfix-package">Setja upp bráðabót lýsigagna</a>.</li>
<li><a href="/dynamics365/operations/dev-itpro/deployment/create-apply-deployable-package">Stofna virkjanlegan pakka</a> sem inniheldur <strong>SCMMobile</strong> líkanið og hlaða síðan virkjanlega pakkann í LCS.</li>
<li><a href="/dynamics365/operations/dev-itpro/deployment/apply-deployable-package-system">Setja virkjanlega pakkann</a> í þitt Microsoft Dynamics 365 fyrir Operations kerfið.</li>
</ol></td>
</tr>
<tr class="odd">
<td>Fartækjavinnusvæðið <strong>Sölupantanir</strong> þarf að vera útgefið í farsímaforrit Dynamics 365 for Operations.</td>
<td>Kerfisstjóri</td>
<td><ol>
<li>Opnaðu Dynamics 365 fyrir Operations í vafranum þínum.</li>
<li>Á <strong>kerfisfæribreytum</strong> síðunni, veljið <strong>Stjórna fartækja vinnusvæði</strong>.</li>
<li>Veljið vinnusvæðið <strong>Sölupantanir</strong>.</li>
<li>Klikkaðu á <strong>Birta fartækjavinnusvæði</strong>.</li>
</ol></td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-dynamics-365-for-operations-mobile-app"></a>Sæktu og settu upp Dynamics 365 fyrir Operations farsímaforrit
Sæktu forritið Microsoft Dynamics 365 fyrir Operations úr forritaverslun farsímans og settu það upp.

-   Fyrir Android: [Dynamics 365 fyrir Operations í Google Play Store](https://play.google.com/store/apps/details?id=com.microsoft.dynamics365.operations.mobile)
-   Fyrir iPhone: [Dynamics 365 fyrir Operations í iTunes forrita versluninni](https://itunes.apple.com/us/app/dynamics-365-for-operations/id1180836730?mt=8)

## <a name="sign-in-to-the-dynamics-365-for-operations-mobile-app"></a>Skráðu þig inn í Dynamics 365 fyrir Operations farsímaforritið
1.  Ræstu forritið í fartækinu þínu.
2.  Skrifaðu þitt Dynamics 365 fyrir Operations vefslóð.
3.  Skráðu fyrirtækið sem á að skrá sig inn á . Til dæmis: Færið inn **USMF**.
4.  Fyrsta skipti sem þú skráir þig inn verðurðu beðin um notandanafn og aðgangsorð fyrir þinn Microsoft Dynamics 365 fyrir Operations reikning. Færðu inn skilríki
5.  Eftir að þú skrá inn, sérðu tiltækt vinnusvæði fyrir Þitt fyrirtæki. Athugið að ef kerfisstjóra gefur út nýja vinnusvæði síðar, geturðu togað til að uppfæra listann yfir fartækja vinnusvæði. 

    [![Togið upp til að uppfæra](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)

## <a name="view-information-about-sales-orders-for-a-customer-by-using-the-mobile-workspace"></a>Skoða upplýsingar um sölupantanir fyrir viðskiptavin með því að nota fartækjavinnusvæðið
1.  Í farsímanum velurðu vinnusvæðið **Sölupantanir**.
2.  Veldu **Skoða pantanir fyrir viðskiptavin**.
3.  Notið lykil eða nafn viðskiptavinar til að finna viðskiptavininn.
4.  Velja viðskiptavin.
5.  Veldu **Tengslaupplýsingar** eða **Sölupantanir**. Ef **Sölupantanir** er valið birtist listi yfir sölupantanir fyrir viðskiptavininn.
6.  Veldu **Velja sölupöntun**. Hér er hægt að skoða upplýsingar um sölupöntunarlínur, sendingar, tengslaupplýsingar viðskiptavinar og tengslaupplýsingar þess sem pantar.





