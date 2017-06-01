---
title: "Heimasíða fartækjaforrits Microsoft Dynamics 365 for Operations"
description: "Þetta efnisatriði lýsir Microsoft Dynamics 365 for Operations farsímaforritinu og veitir tengla á tilföng sem geta hjálpað til við að taka það upp í fyrirtæki."
author: sericks007
manager: AnnBe
ms.date: 04/10/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, Developer, IT Pro
ms.reviewer: annbe
ms.search.scope: Operations, Platform
ms.custom: 272853
ms.assetid: c99f818f-27b3-4e45-92b4-74272dad0e17
ms.search.region: Global
ms.author: sericks
ms.dyn365.ops.intro: Platform update 4
ms.search.validFrom: 2017-02-28
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 5962fa36b061382e7f0ad55c08c81ac2cebc047d
ms.contentlocale: is-is
ms.lasthandoff: 05/25/2017


---

# <a name="dynamics-365-for-operations-mobile-app-home-page"></a>Heimasíða fartækjaforrits Microsoft Dynamics 365 for Operations

[!include[banner](../includes/banner.md)]


Þetta efnisatriði lýsir Microsoft Dynamics 365 for Operations farsímaforritinu og veitir tengla á tilföng sem geta hjálpað til við að taka það upp í fyrirtæki.

<a name="overview"></a>Yfirlit
--------

Microsoft Dynamics 365 fyrir Operations farsímaforritið gerir fyrirtæki þínu kleift til sýna viðskiptaferli þess á fartækjum. Eftir að upplýsingatæknistjórinn þinn opnar vinnusvæði á fartækjum fyrir fyrirtækið, geta notendur skráð sig inn í forritið og strax byrjað að keyra viðskiptaferli úr þeirra fartækjum. Dynamics 365 fyrir Operations farsímaforritið er með eftirfarandi eiginleika, sem geta hjálpað við að auka framleiðni:

-   Notendur geta skoðað, breytt og brugðist við viðskiptagögnin, jafnvel þótt netsamband fartækja þeirra sé óreglulegt eða ekkert. Þegar tæki tengist neti á ný hlaðast upplýsingar um aðgerðir, sem gerðar voru utan nets, upp sjálfvirkt með Dynamics 365 fyrir Operations.
-   Upplýsingatæknistjóri eða forritarar geta byggja og birtið fartækja vinnusvæði sem hefur verið sniðið að þeirra fyrirtæki. Farsímaforritið notar fyrirliggjandi kóða eigna þinna. Þess vegna þarf ekki að færa aftur inn villuleitaraðferðir, viðskiptagrunninn eða öryggis samskipan.
-   Upplýsingatæknistjórar eða forritarar geta auðveldlega hannað fartækja vinnusvæði fyrir fyrirtæki, með því að nota benda-og-smella verkfærið sem er í netútgáfu Dynamics 365 fyrir Operations.
-   Upplýsingatæknistjórar eða forritarar geta einnig hámarka notkun vinnusvæða utan nets með því að nota Business viðskiptagrunn umgjörðina. Þar sem gögn heldur áfram að vinna þegar tæki er utan nets, eru þín farsímaforrit áfram virk og auðug, jafnvel þó ekki tæki hafa tengingu við fasta net.

## <a name="elements-of-the-mobile-app"></a>Einingar farsímaforritsins
Notkun farsímaforritsins samanstendur af fjórum einfalt hugtök: Yfirlit, vinnusvæði, síður og aðgerðir. 

[![Notkunarhugtök í farsímaforritinu](./media/mobilephoneapp1-1024x536.png)](./media/mobilephoneapp1.png)

-   Þegar þú ræsir smáforritið, er farið í **Yfirlitið**.
-   Á upphafsyfirlitinu, er hægt að sjá lista yfir **vinnusvæði** sem birtast í þínu Dynamics 365 fyrir Operations umhverfi.
-   Í hverri vinnusvæði getur séð lista yfir **síður** sem eru tiltæk fyrir það vinnusvæðisins.
-   Á síðu er hægt að skoða gögn sem safnað er úr einni eða fleiri síður í Dynamics 365 fyrir Operations.
-   Á einni síðu er hægt að opna aðrar síður og sjá tengd gögn, eins og upplýsingar um einingu eða línur.
-   Á síðu er einnig hægt að skoða lista yfir **aðgerðir** sem eru tiltækar fyrir þá síðu.
-   Aðgerðir gera það mögulegt að stofna eða breyta fyrirliggjandi gögnum.

## <a name="implementation-process"></a>Innleiðingarverk
Eftirfarandi skýringarmynd sýnir ferlið fyrir innleiðing Dynamics 365 fyrir Operations farsímaforrit í fyrirtækinu þínu. 

![Innleiðingarferli farsímaforrita](./media/mobile-implementation-process_4.png)

Þessi tafla veitir tengla á tilföng sem geta hjálpað til við að útfæra Dynamics 365 fyrir Operations farsímaforrit í fyrirtækið þitt. Tölurnar í fyrsta dálkinum samsvara tölusettu skrefin í síðustu skýringarmynd.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th>Þrep</th>
<th>Hlutverk</th>
<th>Aðgerð</th>
<th>Tilföng til að hjálpa til við að ljúka aðgerð</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>1</td>
<td>Kerfisstjóri</td>
<td>Innleiða Dynamics 365 fyrir Operations í fyrirtækinu.</td>
<td>Ef ekki er þegar Dynamics 365 fyrir Operations starfrækt í fyrirtækinu, sjáið þá <a href="../deployment/deploy-demo-environment.md">Innleiðslu Microsoft Dynamics 365 fyrir Operations sýnigögn í prófunarumhverfi</a>.</td>
</tr>
<tr class="even">
<td>2</td>
<td>Kerfisstjóri</td>
<td>Sæktu og settu upp KBs sem gera kleift að nota fartækja vinnusvæði sem eru veitt af Microsoft.</td>
<td>Finna &quot;Skilyrði&quot; hlutann í efnisatriðum um fartækja vinnusvæði sem fyrirtækið þitt vill nota:
<ul>
<li><a href="/dynamics365/operations/financials/cost-accounting/cost-controlling-mobile-workspace">Fartækjavinnusvæði kostnaðarstýringar</a></li>
<li><a href="/dynamics365/operations/supply-chain/inventory/inventory-on-hand-mobile-workspace">Birgðir á lager fartækjavinnusvæði</a></li>
<li><a href="/dynamics365/operations/supply-chain/sales-marketing/sales-orders-mobile-workspace">Sölupantanir fartækjavinnusvæði</a></li>
<li><a href="/dynamics365/operations/supply-chain/procurement/vendor-collaboration-mobile-workspace">Fartækjavinnusvæði samstarfs lánardrottna</a></li>
<li><a href="/dynamics365/operations/financials/project-management/project-time-entry-mobile-workspace">Vinnustundafærsla verks á fartækjavinnusvæði</a></li>
<li><a href="/dynamics365/operations/financials/expense-management/expense-management-mobile-workspace">Útgjaldastjórnunar fartækja vinnusvæði</a></li>
</ul></td>
</tr>
<tr class="odd">
<td>3</td>
<td>Kerfisstjóri</td>
<td>Gefa út fartækja vinnusvæði sem eru veitt af Microsoft.</td>
<td><a href="publish-mobile-workspace.md">Birta fartækjavinnusvæði</a>
</td>
</tr>
<tr class="even">
<td>4</td>
<td>Forritari eða óháður hugbúnaðarsali (ÓHS)</td>
<td>Nota Dynamics 365 fyrir Operations fartækja umgjörðina til að stofna sérsniðin fartækja vinnusvæði.</td>
<td><ul>
<li><a href="mobile-platform.md">Dynamics 365 fyrir Operations fartækja umgjörð</a></li>
<li><a href="http://ax.help.dynamics.com/en/wiki/operations-mobile-workspace-x-apis/">Dynamics 365 fyrir Operations vinnusvæði X++ APIs</a></li>
</ul></td>
</tr>
<tr class="odd">
<td>5</td>
<td>ÓHS</td>
<td>Stofna virkjanlegan pakka sem inniheldur sérsniðin fartækja vinnusvæði og hala pakkanum upp í Microsoft Dynamics Lifecycle Services (LCS).</td>
<td><a href="../deployment/create-apply-deployable-package.md">Mynda virkjanlegan pakka</a></td>
</tr>
<tr class="even">
<td>6</td>
<td>Kerfisstjóri</td>
<td>Nota virkjanlegan pakka sem inniheldur á sérsniðnum vinnusvæði sem eru veitt af ISV.</td>
<td><a href="../deployment/apply-deployable-package-system.md">Nota virkjanlegan pakka í Microsoft Dynamics 365 fyrir Operations kerfið</a></td>
</tr>
<tr class="odd">
<td>7</td>
<td>Kerfisstjóri</td>
<td>Gefa út sérsniðið fartækja vinnusvæði sem veitt eru af ISV.</td>
<td><a href="publish-mobile-workspace.md">Birta fartækjavinnusvæði</a></td>
</tr>
<tr class="even">
<td>8</td>
<td>Notandi</td>
<td>Sæktu og settu upp fyrir Dynamics 365 for Operations farsímaforritið.</td>
<td><ul>
<li>Fyrir Android: <a href="https://play.google.com/store/apps/details?id=com.microsoft.dynamics365.operations.mobile">Dynamics 365 fyrir Operations í Google Play versluninni</a></li>
<li>Fyrir iPhone: <a href="https://itunes.apple.com/us/app/dynamics-365-for-operations/id1180836730?mt=8">Dynamics 365 fyrir Operations í iTunes forritaversluninni</a></li>
</ul></td>
</tr>
<tr class="odd">
<td>9</td>
<td>Notandi</td>
<td>Sæktu og settu upp fyrir Dynamics 365 for Operations farsímaforritið. Í farsímaforritinu eru fartækja vinnusvæði sem hafa verið gefin út.</td>
<td>Til að skoða lista yfir fartækjavinnusvæði sem í boði eru hjá Microsoft, sjá <a href="mobile-workspaces-released.md">Nýlega útgefin fartækjavinnusvæði fyrir farsímaforritið Dynamics 365 for Operations</a>
</td>
</tr>
</tbody>
</table>






