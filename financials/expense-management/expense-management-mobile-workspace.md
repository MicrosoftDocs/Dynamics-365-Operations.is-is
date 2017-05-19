---
title: "Kostnaðarstýring fartækja vinnusvæði"
description: "Þetta efnisatriði veitir upplýsingar um útgjaldastýringu fartækjavinnusvæði, sem er tiltæk fyrir Microsoft Dynamics 365 fyrir Operations farsímaforrit. Þessi vinnusvæði gerir notendum kleift að ná í kvittun, sem hægt er að tengja við kostnaðarskýrslu síðar. Farsímaforrit vinnusvæði einnig gerir notendum kleift að stofna færslulína með viðhengdri kvittun."
author: annbe
manager: AnnBe
ms.date: 04/10/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: end user, IT Pro
ms.reviewer: annbe
ms.search.scope: Operations
ms.custom: 274023
ms.assetid: 3605eda1-a7ed-4675-8031-5279c5a8f5e4
ms.search.region: Global
ms.author: annbe
ms.dyn365.ops.intro: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: Human Translation
ms.sourcegitcommit: 8bc47c5b170fd7dd8f6288682aad6eae1d2dc09a
ms.openlocfilehash: 9d3b7a4d5184c3c4958f4298f1d3dd4de0cd06d6
ms.contentlocale: is-is
ms.lasthandoff: 04/26/2017


---

# <a name="expense-management-mobile-workspace"></a>Kostnaðarstýring fartækja vinnusvæði

[!include[banner](../includes/banner.md)]

"[!include[banner](../includes/banner.md)]"


Þetta efnisatriði veitir upplýsingar um útgjaldastýringu fartækjavinnusvæði, sem er tiltæk fyrir Microsoft Dynamics 365 fyrir Operations farsímaforrit. Þessi vinnusvæði gerir notendum kleift að ná í kvittun, sem hægt er að tengja við kostnaðarskýrslu síðar. Farsímaforrit vinnusvæði einnig gerir notendum kleift að stofna færslulína með viðhengdri kvittun.

<a name="overview-of-the-expense-management-mobile-workspace"></a>Yfirlit yfir útgjaldastjórnun í fartækjasvæði
---------------------------------------------------

Mörg fyrirtæki þurfa afrit af kvittun í viðhengi, sem sýnir útgjöld í ferðalög eða viðskipti sem tengjast kostnaðarskýrsluna sem starfsmaður sendi til að fá endurgreiðslu. **Útgjaldastjórnun** fartækjasvæðið gerir notendum kleift að stofna nýja færslulínur í fartæki að hans vali með því að nota í viðhengi mynd af kvittun. Einnig geta notendur safna myndum af kvittun og síðan tengið hana kostnaðarskýrslu síðar. Nánar til tekið, **útgjaldastjórnun** fartækjavinnusvæði gerir notanda kleift að:

-   Taka mynd af kvittun og hlaða inn á Microsoft Dynamics 365 fyrir Operations. Notandi getur svo tengja myndina við kostnaðarskýrslu seinna.
-   Senda inn skrá sem fönguð kvittun. Notandi getur svo viðhengt sem mynd í kostnaðarskýrslu seinna.
-   Stofna nýja línu í kostnaðarskýrslu með því að nota viðhengda kvittun. Notandi getur svo bætt línuatriði við kostnaðarskýrslu síðar og sent hana til samþykktar og endurgreiðslu.

Þeir hlutar sem eftir eru í þessu efnisatriði útskýra hvernig á að innleiða og nota **útgjaldastýringu** á færtækja vinnusvæðinu.

## <a name="prerequisites"></a>Frumskilyrði
Áður en hægt er að nota **útgjaldastýringu** í fartækja vinnusvæði gangið úr skugga um að kerfisstjórinn hafi tryggt eftirfarandi forsendur.

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
<td>Ef Dynamics 365 fyrir Operations er ekki enn starfrækt í fyrirtækinu, skal kerfisstjórinn <a href="http://ax.help.dynamics.com/en/wiki/deploy-an-ax7-demo-environment/">setja upp Microsoft Dynamics 365 fyrir Operations í prófunarumhverfi</a>.</td>
</tr>
<tr class="even">
<td>KB 4019015 verður að vera innleitt.</td>
<td>Kerfisstjóri</td>
<td>KB 4019015 (X++ uppfærsla eða lýsigögn bráðabót) inniheldur fjögur fartækja vinnusvæði fyrir birgðakeðjustjórnun. Áður en KB 4019015 er sett upp, verður kerfisstjóri að fylgja eftirfarandi skrefum:
<ol>
<li>Sækja KB 4019015 af Microsoft Dynamics Lifecycle Services (LCS).</li>
<li><a href="https://ax.help.dynamics.com/en/wiki/configuring-and-installing-a-metadata-hotfix-package/">Setja upp bráðabót lýsigagna</a>.</li>
<li><a href="https://ax.help.dynamics.com/en/wiki/create-and-apply-a-deployable-package/">Stofna virkjanlegan pakka</a> sem inniheldur <strong>ApplicationSuite</strong> og <strong>ExpenseMobile</strong> virðislíkön og hlaða svo upp virkjanlegum pakka í LCS.</li>
<li><a href="https://ax.help.dynamics.com/en/wiki/apply-a-deployable-package-on-a-dynamics-ax-system/">Setja virkjanlega pakkann</a> í þitt Microsoft Dynamics 365 fyrir Operations kerfið.</li>
</ol></td>
</tr>
<tr class="odd">
<td><strong>Útgjaldastýring</strong> fartækjavinnusvæðið verður að vera sett upp í Dynamics 365 fyrir Operations farsímaforritinu.</td>
<td>Kerfisstjóri</td>
<td><ol>
<li>Opnaðu Dynamics 365 fyrir Operations í vafranum þínum.</li>
<li>Á <strong>kerfisfæribreytum</strong> síðunni, veljið <strong>Stjórna fartækja vinnusvæði</strong>.</li>
<li>Veljið Vinnusvæðið <strong>Útgjaldastýring</strong>.</li>
<li>Klikkaðu á <strong>Birta fartækjavinnusvæði</strong>.</li>
</ol></td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-dynamics-365-for-operations-mobile-app"></a>Sæktu og settu upp Dynamics 365 fyrir Operations farsímaforrit
Sæktu forritið Microsoft Dynamics 365 fyrir Operations úr forritaverslun farsímans og settu það upp.

-   Fyrir Android: [Dynamics 365 fyrir Operations í Google Play Store](https://play.google.com/store/apps/details?id=com.microsoft.dynamics365.operations.mobile)
-   Fyrir iPhone: [Dynamics 365 fyrir Operations í iTunes forrita versluninni](https://itunes.apple.com/us/app/dynamics-365-for-operations/id1180836730?mt=8)
-   Fyrir Windows síma (Universal Windows Svæði \[UWP\]): Kemru á næstunni!

## <a name="sign-in-to-the-dynamics-365-for-operations-mobile-app"></a>Skráðu þig inn í Dynamics 365 fyrir Operations farsímaforritið
1.  Ræstu forritið í fartækinu þínu.
2.  Skrifaðu þitt Dynamics 365 fyrir Operations vefslóð.
3.  Skráðu fyrirtækið sem á að skrá sig inn á . Til dæmis: Færið inn **USMF**.
4.  Fyrsta skipti sem þú skráir þig inn verðurðu beðin(n) um notandanafn og aðgangsorð fyrir þinn Microsoft Dynamics 365 fyrir Operations reikning. Færðu inn skilríki
5.  Eftir að þú skrá inn, sérðu tiltækt vinnusvæði fyrir Þitt fyrirtæki. Athugið að ef kerfisstjóra gefur út nýtt vinnusvæði síðar, er hægt að endurræsa listann yfir fartækja vinnusvæði. [![Togið upp til að uppfæra](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)

## <a name="capture-a-receipt-by-using-the-expense-management-mobile-workspace"></a>Fangaðu kvittun á fartækjavinnusvæðinu með Útgjaldastjórnun
1.  Í farsímanum velurðu **Útgjaldastjórnunar** vinnusvæðið.
2.  Velja **Föngun kvittunar**.
3.  Veljið **Taka mynd** eða **Velja mynd**.
4.  Ef valið er **Taka mynd**, skal fylgja þessum skrefum:
    1.  Þú færist yfir á myndavél á fartækinu þínu, svo þú getir tekið mynd af kvittuninni. Þegar búið er að taka mynd, klikkaðu á **í lagi** til að samþykkja myndina.
    2.  Valfrjálst: Sláðu inn nafn myndarinnar og færðu inn þær athugasemdir sem þarf.

     Eða Ef þú er velur **Veljið mynd**, skal fylgja þessum skrefum:
    1.  Í listanum skal velja mynd.
    2.  Valfrjálst: Sláðu inn nafn myndarinnar og færðu inn þær athugasemdir sem þarf.

5.  Velja **Ekkert**.

## <a name="quick-expense-entry-by-using-the-expense-management-mobile-workspace"></a>Snögg færsla útgjalda með því að nota Útgjaldastýring á fartækja vinnusvæði
1.  Í farsímanum velurðu **Útgjaldastjórnunar** vinnusvæðið.
2.  Veljið **Útgjöld snögg færsla**.
3.  Velja tegund fyrir útgjöldin. Þá sérðu lista yfir vörur sem er hlaðið upp í forritið til notkunar utan nets. 50 atriðum er hlaðið sjálfgefið en þeirri tölu má breyta af forritara. Forritarar nálgist nánari upplýsingar í [Dynamics 365 fyrir Operations á fartækja svæði](http://ax.help.dynamics.com/en/wiki/mobile-development-handbook/). Ef þinn flokkur er ekki á listanum skal velja **Leita áfram** til að framkvæma leit á netinu í Dynamics 365 fyrir Operations. Leita eftir flokki útgjalda eða skipta til að leita eftir tegund útgjalda.
4.  Færa inn dagsetningu færslu útgjaldanna.
5.  Valfrjálst: Færið inn söluaðila kostnaðar.
6.  Færið inn útgjaldaupphæð.
7.  Veljið gjaldmiðilskóðann fyrir úgjöldin. Þá sérðu lista yfir vörur sem er hlaðið upp í forritið til notkunar utan nets. 400 atriðum er hlaðið sjálfgefið en þeirri tölu má breyta af forritara. Forritarar nálgist nánari upplýsingar í [Dynamics 365 fyrir Operations á fartækja svæði](http://ax.help.dynamics.com/en/wiki/mobile-development-handbook/). Ef gjaldmðill er ekki á listanum skal velja **Leita áfram** til að framkvæma leit á netinu í Dynamics 365 fyrir Operations. Leita eftir gjaldmiðli eða skipta til að leita eftir nafni.
8.  Veljið **Taka mynd** eða **Velja mynd**.
9.  Ef þú valdir **Taka mynd**, ertu færður yfir á myndavél fartækisins, svo þú getir myndað kvittunina. Þegar búið er að taka mynd, klikkaðu á **í lagi** til að samþykkja myndina.  Eða Ef þú valdir **Velja mynd**, velurðu mynd af listanum.
10. Velja **Ekkert**.






