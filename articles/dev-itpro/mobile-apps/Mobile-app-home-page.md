---
title: "Heimasíða fyrir Dynamics 365 for Unified Operations-farsímaforrit"
description: "Þetta efnisatriði lýsir Microsoft Dynamics 365 for Unified Operations fartækjaforritinu og veitir tengla á tilföng sem geta hjálpað til við að taka það upp í fyrirtæki."
author: sericks007
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.custom: 272853
ms.assetid: c99f818f-27b3-4e45-92b4-74272dad0e17
ms.search.region: Global
ms.author: sericks
ms.dyn365.ops.version: Platform update 4
ms.search.validFrom: 2017-02-28
ms.translationtype: HT
ms.sourcegitcommit: 96a9075294c1f2a9cfde03be1aaaa26af90de4c2
ms.openlocfilehash: d6d26da330974305fa3725fe7c2506d198b17e2c
ms.contentlocale: is-is
ms.lasthandoff: 09/04/2018

---

# <a name="dynamics-365-for-unified-operations-mobile-app-home-page"></a>Heimasíða fyrir Dynamics 365 for Unified Operations-farsímaforrit

[!include [banner](../includes/banner.md)]

Þetta efnisatriði lýsir Microsoft Dynamics 365 for Unified Operations fartækjaforritinu og veitir tengla á tilföng sem geta hjálpað til við að taka það upp í fyrirtæki.

> [!NOTE]
> Fartækjaforritið hét áður *Microsoft Dynamics 365 for Finance and Operations*.

<a name="overview"></a>Yfirlit
--------

Fartækjaforritið gerir fyrirtæki þínu kleift að gera viðskiptaferla aðgengilega á fartækjum. Eftir að upplýsingatæknistjóri þinn opnar vinnusvæði á fartækjum fyrir fyrirtækið, geta notendur skráð sig inn í forritið og strax byrjað að keyra viðskiptaferli úr þeirra fartækjum. Fartækjaforritið er með eftirfarandi eiginleika, sem geta hjálpað við að auka framleiðni:

- Notendur geta skoðað, breytt og brugðist við viðskiptagögnin, jafnvel þótt netsamband fartækja þeirra sé óreglulegt eða ekkert. Þegar tæki tengist neti á ný hlaðast upp upplýsingar um aðgerðir, sem gerðar voru utan nets, sjálfvirkt með Dynamics 365 for Finance and Operations.
- Upplýsingatæknistjóri eða forritarar geta byggja og birtið fartækja vinnusvæði sem hefur verið sniðið að þeirra fyrirtæki. Farsímaforritið notar fyrirliggjandi kóða eigna þinna. Þess vegna þarf ekki að færa aftur inn villuleitaraðferðir, viðskiptagrunninn eða öryggis samskipan.
- Upplýsingatæknistjórar eða forritarar geta auðveldlega hannað fartækjavinnusvæði með því að nota benda-og-smella verkfærið sem er í vefbiðlaranum.
- Upplýsingatæknistjórar eða forritarar geta einnig hámarka notkun vinnusvæða utan nets með því að nota Business viðskiptagrunn umgjörðina. Þar sem gögn heldur áfram að vinna þegar tæki er utan nets, eru þín farsímaforrit áfram virk og auðug, jafnvel þó ekki tæki hafa tengingu við fasta net.

## <a name="elements-of-the-mobile-app"></a>Einingar farsímaforritsins
Fletting í fartækjaforritinu byggist á fjórum meginhugtökum: mælaborði, vinnusvæðum, síðum og aðgerðum. 

[![Notkunarhugtök í farsímaforritinu](./media/mobilephoneapp1-1024x536.png)](./media/mobilephoneapp1.png)

1. Þegar þú ræsir smáforritið, er farið í **Yfirlitið**.
2. Á mælaborðinu getur þú séð lista yfir **vinnusvæði** sem hafa verið gefin út.
3. Í hverri vinnusvæði getur séð lista yfir **síður** sem eru tiltæk fyrir það vinnusvæðisins.
4. Hægt er að framkvæma ýmsar aðgerðir á síðu. Hér eru nokkur dæmi:

    - Skoða ítarleg gögn.
    - Fletta á aðrar síður fyrir tengd gögn, eins og einingaupplýsingar eða línur.
    - Sjá lista yfir **aðgerðir** sem eru tiltækar fyrir þá síðu. Aðgerðir gera það mögulegt að stofna eða breyta fyrirliggjandi gögnum.

## <a name="implementation-process"></a>Innleiðingarverk
Eftirfarandi skýringarmynd sýnir ferlið fyrir innleiðingu á bæði fartækjavinnusvæðum frá Microsoft og sérsniðnum fartækjavinnusvæðum. 

![Innleiðingarferli farsímaforrita](./media/Mobile-implementation-process-5.png)

Eftirfarandi tafla inniheldur tengla á tilföng sem geta hjálpað til við að innleiða bæði fartækjavinnusvæði frá Microsoft og sérsniðin fartækjavinnusvæði. Tölurnar í fyrsta dálkinum samsvara tölusettu skrefin í síðustu skýringarmynd.

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
<td>Innleiða Finance and Operations í þitt fyrirtæki.</td>
<td><ul><li>Ef þú hefur ekki enn notað útgáfu af Microsoft Dynamics 365 skaltu sjá <a href="../deployment/deploy-demo-environment.md">Virkja sýniútgáfuumhverfi</a>.</li><li>Lista yfir fartækjavinnusvæði sem hægt er að nota má sjá á <a href="mobile-workspaces-released.md">Fartækjavinnusvæði, nýlega útgefin</a>.</li></ul></td>
</tr>
<tr class="even">
<td>2</td>
<td>Kerfisstjóri</td>
<td><strong>Ef þú notar Microsoft Dynamics 365 for Operations útgáfu 1611:</strong> Sæktu og settu upp KBs sem gera kleift að nota fartækjavinnusvæði sem Microsoft útvegar.</td>
<td>Sjáðu eftirfarandi efnisatriði til að fá frekari upplýsingar:
<ul>

<li><a href="../../financials/cost-accounting/cost-controlling-mobile-workspace.md">Fartækjavinnusvæði kostnaðarstýringar</a></li>
<li><a href="../../supply-chain/inventory/inventory-on-hand-mobile-workspace.md">Birgðir á lager eftir fartækjavinnusvæði</a></li>
<li><a href="../../supply-chain/sales-marketing/sales-orders-mobile-workspace.md">Sölupantanir fartækjavinnusvæði</a></li>
<li><a href="../../supply-chain/procurement/vendor-collaboration-mobile-workspace.md">Fartækjavinnusvæði samstarfs lánardrottna</a></li>
<li><a href="../../financials/project-management/project-time-entry-mobile-workspace.md">Vinnustundafærsla verks á fartækjavinnusvæði</a></li>
<li><a href="../../financials/expense-management/expense-management-mobile-workspace.md">Fartækjavinnusvæði útgjaldastýringar</a></li>

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
<td>Nota fartækja umgjörðina til að stofna sérsniðin fartækja vinnusvæði.</td>
<td><a href="platform/mobile-platform-home-page.md">Fartækjaverkvangur</a></td>
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
<td>Notaðu virkjanlega pakkann sem inniheldur sérsniðin vinnusvæði frá óháðum hugbúnaðarsala (ISV).</td>
<td><a href="../deployment/apply-deployable-package-system.md">Virkjanlegur pakki notaður</a></td>
</tr>
<tr class="odd">
<td>7</td>
<td>Kerfisstjóri</td>
<td>Gefa út sérsniðið fartækja vinnusvæði sem veitt eru af ISV.</td>
<td><a href="publish-mobile-workspace.md">Fartækjavinnusvæði birt</a></td>
</tr>
<tr class="even">
<td>8</td>
<td>Notandi</td>
<td>Sæktu og settu upp fartækjaforritið.</td>
<td>
<a href="https://go.microsoft.com/fwlink/?linkid=850662">Unified Operations-forrit fyrir Android</a><BR/>
<a href="https://go.microsoft.com/fwlink/?linkid=850663">Unified Operations-forrit fyrir IOS</a><BR/>
(Styður ekki Windows Phone)
</td>
</tr>
<tr class="odd">
<td>9</td>
<td>Notandi</td>
<td>Innskráning og notkun fartækjaforritsins. Forritið hefur að geyma fartækjavinnusvæði sem hafa verið gefin út af kerfisstjóra.</td>
<td>Lista yfir fartækjavinnusvæði frá Microsoft má sjá á <a href="mobile-workspaces-released.md">Fartækjavinnusvæði, nýlega útgefin</a>.
</td>
</tr>
</tbody>
</table>

