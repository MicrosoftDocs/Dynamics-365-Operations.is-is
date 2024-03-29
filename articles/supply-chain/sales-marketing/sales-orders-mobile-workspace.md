---
title: Fartækjavinnusvæði sölupantana
description: Þessi grein veitir upplýsingar um fartækjavinnusvæði sölupantana. Þetta vinnusvæði hjálpar þér að hafa yfirsýn yfir sölupantanir þínar hvar og hvenær sem er.
author: Henrikan
ms.date: 05/24/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: 267134
ms.assetid: 0ce96511-002b-4de7-b31e-4303f94edc84
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: henrikan
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: 38971f2a5f3f3d2692de0e52365e2215170101cc
ms.sourcegitcommit: 12b3dbee905f8b2eb2e6c383c822a0fc9fccf063
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 07/01/2022
ms.locfileid: "9103181"
---
# <a name="sales-orders-mobile-workspace"></a>Fartækjavinnusvæði sölupantana

[!include [banner](../includes/banner.md)]
[!include [mobile app deprecation](../../fin-ops-core/dev-itpro/includes/mobile-app-deprecation-banner.md)]

Þessi grein veitir upplýsingar um fartækjavinnusvæðið **Sölupantanir**. Þetta vinnusvæði hjálpar þér að hafa yfirsýn yfir sölupantanir þínar hvar og hvenær sem er. 

Þessu fartækjavinnusvæði er ætlað til að nota með farsímaforritum Fjármála- og reksturs (Dynamics 365) .

## <a name="overview"></a>Yfirlit
Í **sölupantanir** farsímaforrit vinnusvæði gerir það mögulegt að skoða nákvæmar upplýsingar um hverja sölupöntun. Þessar upplýsingar innihalda einnig stöðu pöntunar, upplýsingar fyrir viðskiptavininn og samskiptaupplýsingar fyrir þann sem pantar. Farsímavinnusvæðið **Sölupantanir** veitir fljótlegt yfirlit sölupantana. Hægt er að skoða allar sölupantanir, sölupantanir eftir viðskiptavini, eða skoða upplýsingar um tiltekna sölupöntun. 

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

## <a name="prerequisites"></a>Forkröfur
Skilyrðin eru breytileg, byggt á útgáfu Microsoft Dynamics 365 sem hefur verið sett upp fyrir fyrirtækið þitt.

### <a name="prerequisites-if-you-use-supply-chain-management"></a>Forkröfur ef þú notar Supply Chain Management 
Ef Supply Chain Management hefur verið innleitt í fyrirtækinu verður kerfisstjóri að birta fartækjavinnusvæðið **Sölupantanir**. Leiðbeiningar er að finna í [Fartækjavinnusvæði birt](../../fin-ops-core/dev-itpro/mobile-apps/publish-mobile-workspace.md).

### <a name="prerequisites-if-you-use-dynamics-365-for-operations-version-1611-with-platform-update-3-or-later"></a>Skilyrði ef þú notar Dynamics 365 for Operations útgáfu 1611 með verkvangsuppfærslu 3 eða síðar
Ef Dynamics 365 for Operations útgáfa 1611 með verkvangsuppfærslu 3 eða síðar hefur verið sett upp fyrir fyrirtækið þitt, verður kerfisstjórinn að ljúka eftirfarandi skilyrðum. 

<table>
<thead>
<tr class="header">
<th>Skilyrði</th>
<th>Hlutverk</th>
<th>lýsing</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Innleiða KB 4013633.</td>
<td>Kerfisstjóri</td>

<td>KB 4013633 er X++ uppfærsla eða lýsigagnabráðabót sem inniheldur fartækjavinnusvæðið <strong>Sölupantanir</strong>. Til að setja upp KB 4013633 verður kerfisstjóri að fylgja eftirfarandi skrefum.
<ol>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/download-hotfix-lcs">Sækja bráðabót lýsigagna frá Microsoft Dynamics Lifecycle Services (LCS)</a>.</li>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/install-metadata-hotfix-package">Setja upp bráðabót lýsigagna</a>.</li>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/deployment/create-apply-deployable-package">Stofna virkjanlegan pakka</a> sem inniheldur <strong>SCMMobile</strong> líkanið og hlaða síðan virkjanlega pakkann í LCS.</li>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/deployment/apply-deployable-package-system">Notaðu virkjanlega pakkann</a>.</li>

</ol></td>
</tr>
<tr class="even">
<td>Gefa út á <strong>sölupantanir</strong> farsímaforrit vinnusvæðisins.</td>
<td>Kerfisstjóri</td>
<td>Sjáið <a href="/dynamics365/fin-ops-core/dev-itpro/mobile-apps/publish-mobile-workspace">Fartækjavinnusvæði birt</a>.</td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-mobile-app"></a>Sæktu og settu upp fartækjaforritið
Sækið Fjármála- og rekstrarforrit (Dynamics 365) fyrir fartæki

-   [Fyrir Android síma](https://go.microsoft.com/fwlink/?linkid=850662)
-   [Fyrir iPhone síma](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a>Innskráning í fartækjaforritið

1.  Ræstu forritið í fartækinu þínu.
2.  Færðu inn vefslóð þína fyrir Dynamics 365.
3.  Í fyrsta sinn sem þú skráir þig inn, er beðið um notandanafn og aðgangsorð þitt. Færðu inn skilríki
4.  Eftir að þú hefur skráð þig inn, birtast tiltæk vinnusvæði fyrir fyrirtækið. Athugið að ef kerfisstjóri gefur út nýtt vinnusvæði síðar, verður að endurræsa listann yfir fartækjavinnusvæði.

[![Togið til að uppfæra.](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)

## <a name="view-information-about-sales-orders-for-a-customer-by-using-the-sales-order-mobile-workspace"></a>Skoða upplýsingar um sölupantanir fyrir viðskiptavin með því að nota fartækjavinnusvæðið Sölupantanir

1.  Í farsímanum velurðu vinnusvæðið **Sölupantanir**.
2.  Veldu **Skoða pantanir fyrir viðskiptavin**.
3.  Notið lykil eða nafn viðskiptavinar til að finna viðskiptavininn.
4.  Velja viðskiptavin.
5.  Veldu **Tengslaupplýsingar** eða **Sölupantanir**. Ef **Sölupantanir** er valið birtist listi yfir sölupantanir fyrir viðskiptavininn.
6.  Veldu **Velja sölupöntun**. Hér er hægt að skoða upplýsingar um sölupöntunarlínur, sendingar, tengslaupplýsingar viðskiptavinar og tengslaupplýsingar þess sem pantar.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

