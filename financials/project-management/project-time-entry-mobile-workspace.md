---
title: "Vinnustundafærsla verks á fartækjavinnusvæði fyrir forritið Microsoft Dynamics 365 for Operations"
description: "Þetta efnisatriði veitir upplýsingar um vinnustundafærslu verks á fartækjavinnusvæði. Þessi vinnusvæði gerir notendum kleift að færa inn og vista vinnustundir sem tengist verkefni með því að nota þeirra fartæki."
author: annbe
manager: AnnBe
ms.date: 05/10/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: annbe
ms.search.scope: Operations, Core
ms.custom: 272101
ms.assetid: 4505f021-b9bb-4b87-be24-6bf0bd88ee60
ms.search.region: Global
ms.search.industry: Service industries
ms.author: annbe
ms.dyn365.ops.intro: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 9c592c301908898915164e9236850759b73543fe
ms.contentlocale: is-is
ms.lasthandoff: 05/25/2017


---

# <a name="project-time-entry-mobile-workspace"></a>Vinnustundafærsla verks á fartækjavinnusvæði

[!include[banner](../includes/banner.md)]



Þetta efnisatriði veitir upplýsingar um vinnustundafærslu verks á fartækjavinnusvæði fyrir fartækjaforritið Dynamics 365 for Operations. Þessi vinnusvæði gerir notendum kleift að færa inn og vista vinnustundir sem tengist verkefni með því að nota þeirra fartæki.

<a name="overview-of-the-project-time-entry-mobile-workspace"></a>Yfirlit yfir vinnustundafærslu verks á fartækjavinnusvæði
---------------------------------------------------

Sem hluti af daglegu starfi sínu eru þeir sem sinna verkum oft á staðnum eða á ferðalagi. Fartækjavinnusvæði **Vinnustundafærsla verks** gerir notendum kleift að færa reikninshæfan og ekki reikningshæfan tíma á verk í eigin fartæki. Þar af leiðandi geta tilföng verks skráð vinnustundafærslur hvar og hvenær sem er. Þau geta einnig skoða tímafærslur sem þegar hafa verið skráðar. 

Fartækjavinnusvæði **Vinnustundafærsla verks** tryggir einkum eftirfarandi eiginleika:

-   Fyrir einhverja valda dagsetningu skal færa inn þann fjölda klukkustunda sem var notaður í tiltekið verk.
-   Leita eftir verkheiti eða viðskiptavinum til að finna verk sem slá á inn tíma fyrir.
-   Tilgreina tegund og verkþátt fyrir tímann sem er eytt.
-   Skrá tíma sem reikningshæfan eða ekki reikningshæfan fyrir verk.
-   Einnig er hægt að færa inn innri eða ytri athugasemdir.

Til þess að innleiða fartækjavinnusvæðið **Vinnustundafærsla verks** skal sjá eftirfarandi hluta í þessu efnisatriði.

## <a name="prerequisites"></a>Frumskilyrði
Áður en hægt er að nota **Vinnustundafærsla verks** í fartækja vinnusvæði gangið úr skugga um að kerfisstjórinn hafi tryggt eftirfarandi forsendur.

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
<td>Verður að innleiða Microsoft Dynamics 365 útgáfu 1611 með svæðisuppfærslu 3 eða síðar.</td>
<td>Kerfisstjóri</td>
<td>Ef Dynamics 365 fyrir Operations er ekki enn starfrækt í fyrirtækinu, skal kerfisstjórinn <a href="/dynamics365/operations/dev-itpro/deployment/deploy-demo-environment">setja upp Microsoft Dynamics 365 fyrir Operations í prófunarumhverfi</a>.</td>
</tr>
<tr class="even">
<td>KB 4018050 verður að vera innleitt.</td>
<td>Kerfisstjóri</td>
<td>KB 4018050 er X++ uppfærsla eða bráðabót lýsingagna sem inniheldur fartækjavinnusvæði <strong>Vinnustundafærsla verks</strong>. Til að setja upp KB 4018050 verður kerfisstjóri að fylgja eftirfarandi skrefum.
<ol>
<li>Sækja KB 4018050 af Microsoft Dynamics Lifecycle Services (LCS).</li>
<li><a href="/dynamics365/operations/dev-itpro/migration-upgrade/install-metadata-hotfix-package">Setja upp bráðabót lýsigagna</a>.</li>
<li><a href="/dynamics365/operations/dev-itpro/deployment/create-apply-deployable-package">Stofna virkjanlegan pakka</a> sem inniheldur <strong>ApplicationSuite</strong> og <strong>ProjectMobile</strong> virðislíkön og hlaða svo upp virkjanlegum pakka í LCS.</li>
<li><a href="/dynamics365/operations/dev-itpro/deployment/apply-deployable-package-system">Setja virkjanlega pakkann</a> í þitt Microsoft Dynamics 365 fyrir Operations kerfið.</li>
</ol></td>
</tr>
<tr class="odd">
<td>Fartækjavinnusvæðið <strong>Vinnustundafærsla verks</strong> þarf að vera útgefið í farsímaforriti Dynamics 365 for Operations.</td>
<td>Kerfisstjóri</td>
<td><ol>
<li>Opnaðu Dynamics 365 fyrir Operations í vafranum þínum.</li>
<li>Á síðunni <strong>Kerfisfæribreytur</strong> á flipanum <strong>Stjórna fartækjavinnusvæði</strong> skal velja vinnusvæðið <strong>Vinnustundafærsla verks</strong>.</li>
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
4.  Fyrsta skipti sem þú skráir þig inn verðurðu beðin um notandanafn og aðgangsorð fyrir þinn Dynamics 365 for Operations reikning. Færðu inn skilríki
5.  Eftir að þú skrá inn, sérðu tiltækt vinnusvæði fyrir Þitt fyrirtæki. Athugið að ef kerfisstjóra gefur út nýtt vinnusvæði síðar, er hægt að endurræsa listann yfir fartækja vinnusvæði.

[![Togið upp til að uppfæra](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)

## <a name="enter-time-by-using-the-project-time-entry-mobile-workspace"></a>Færið inn tíma með því að nota í fartækjavinnusvæðið Vinnustundafærsla verks
1.  Í farsímanum velurðu vinnusvæðið **Vinnustundafærsla verks**.
2.  Veljið **Vinnustundafærsla**. Dagatalsdagsetningar sjást fyrir gildandi viku.
3.  Fyrir valda dagsetningu skal velja **Aðgerðir** &gt; **Ný færsla**.
4.  Færið inn fjölda klukkustunda.
5.  Veljið verkið fyrir vinnustundafærsluna. Þá sérðu lista yfir vörur sem er hlaðið upp í forritið til notkunar utan nets. 50 atriðum er hlaðið sjálfgefið en þeirri tölu má breyta. Forritarar ættu að skoða [Farsímaforrit fyrir Dynamics 365 for Operations](/dynamics365/operations/dev-itpro/mobile-apps/mobile-platform).
6.  Ef verkið þitt er ekki á listanum skal velja **Leita** til að framkvæma leit á netinu í Dynamics 365 for Operations. Leita eftir nafni eða skipta yfir í leit til að leita eftir nafni eða viðskiptavini.
7.  Veljið tegund. Þá sérðu lista yfir vörur sem er hlaðið upp í forritið til notkunar utan nets. 50 atriðum er hlaðið sjálfgefið en þeirri tölu má breyta. Forritarar ættu að skoða [Farsímaforrit fyrir Dynamics 365 for Operations](/dynamics365/operations/dev-itpro/mobile-apps/mobile-platform).
8.  Ef þinn flokkur er ekki á listanum skal velja **Leita áfram** til að framkvæma leit á netinu í Dynamics 365 fyrir Operations. Leita eftir tegund eða skipta til að leita að nafni tegundar.
9.  Velja verkþátt. Þá sérðu lista yfir vörur sem er hlaðið upp í forritið til notkunar utan nets. 50 atriðum er hlaðið sjálfgefið en þeirri tölu má breyta. Forritarar ættu að skoða [Farsímaforrit fyrir Dynamics 365 for Operations](/dynamics365/operations/dev-itpro/mobile-apps/mobile-platform).
10. Ef verkþátturinn þinn er ekki á listanum skal velja **Leita** til að framkvæma leit á netinu í Dynamics 365 for Operations. Leita eftir verkþáttarnúmer eða skipta í að leita eftir tilgangi.
11. Velja línueiginleika.
12. Valfrjálst: Færðu inn innri eða ytri athugasemdir.
13. Velja **Ekkert**.






