---
title: "Vinnustundafærsla verks á fartækjavinnusvæði"
description: "Þetta efnisatriði veitir upplýsingar um vinnustundafærslu verks á fartækjavinnusvæði. Þessi vinnusvæði gerir notendum kleift að færa inn og vista vinnustundir sem tengist verkefni með því að nota þeirra fartæki."
author: KimANelson
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 272101
ms.assetid: 4505f021-b9bb-4b87-be24-6bf0bd88ee60
ms.search.region: Global
ms.search.industry: Service industries
ms.author: knelson
ms.dyn365.ops.intro: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: HT
ms.sourcegitcommit: 69eeb90387ca5765c163c7d482295ea104cc078c
ms.openlocfilehash: 2acf5a982988fe00492523ed5ce77d6de4a9e146
ms.contentlocale: is-is
ms.lasthandoff: 09/29/2017

---

# <a name="project-time-entry-mobile-workspace"></a>Vinnustundafærsla verks á fartækjavinnusvæði

[!include[banner](../includes/banner.md)]

Þetta efnisatriði veitir upplýsingar um fartækjavinnusvæðið **Vinnustundafærsla verks**. Þessi vinnusvæði gerir notendum kleift að færa inn og vista vinnustundir sem tengist verkefni með því að nota þeirra fartæki.

Þetta fartækjavinnusvæði er ætlað til notkunar með fartækjaforritinu Microsoft Dynamics 365 for Unified Operations. 

## <a name="overview"></a>Yfirlit
Sem hluti af daglegu starfi sínu eru þeir sem sinna verkum oft á staðnum eða á ferðalagi. Fartækjavinnusvæði **Vinnustundafærsla verks** gerir notendum kleift að færa reikninshæfan og ekki reikningshæfan tíma á verk í eigin fartæki. Þar af leiðandi geta tilföng verks skráð vinnustundafærslur hvar og hvenær sem er. Þau geta einnig skoða tímafærslur sem þegar hafa verið skráðar. 

Nánar tiltekið, í fartækjavinnusvæðinu **Vinnustundafærsla verks** geta notendur framkvæmt þessi verk:

-   Fyrir einhverja valda dagsetningu skal færa inn þann fjölda klukkustunda sem var notaður í tiltekið verk.
-   Leita eftir verkheiti eða viðskiptavinum til að finna verk sem slá á inn tíma fyrir.
-   Tilgreina tegund og verkþátt fyrir tímann sem er eytt.
-   Skrá tíma sem reikningshæfan eða ekki reikningshæfan fyrir verk.
-   Einnig er hægt að færa inn innri eða ytri athugasemdir.

## <a name="prerequisites"></a>Frumskilyrði
Forkröfur eru mismunandi eftir þeirri útgáfu Microsoft Dynamics 365 sem hefur verið innleidd í fyrirtækinu.

### <a name="prerequisites-if-you-use-microsoft-dynamics-365-for-finance-and-operations-enterprise-edition-july-2017"></a>Forkröfur ef þú notar Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition (júlí 2017) 
Ef Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition (júlí 2017) hefur verið beitt í þínu fyrirtæki verður kerfisstjóri að birta fartækjavinnusvæðið **Vinnustundafærsla verks**. Leiðbeiningar er að finna í [Fartækjavinnusvæði birt](../../dev-itpro/mobile-apps/publish-mobile-workspace.md).

### <a name="prerequisites-if-you-use-microsoft-dynamics-365-for-operations-version-1611-with-platform-update-3-or-later"></a>Forkröfur ef verið er að nota Microsoft Dynamics 365 for Operations útgáfu 1611 með svæðisuppfærslu 3 eða síðar
Ef verið er að nota Microsoft Dynamics 365 for Operations útgáfu 1611 með svæðisuppfærslu 3 eða síðar í fyrirtækinu, verður kerfisstjóri að uppfylla eftirfarandi forkröfur. 

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

<td>Innleiða KB 4018050.</td>
<td>Kerfisstjóri</td>
<td>KB 4018050 er X++ uppfærsla eða bráðabót lýsingagna sem inniheldur fartækjavinnusvæði <strong>Vinnustundafærsla verks</strong>. Til að setja upp KB 4018050 verður kerfisstjóri að fylgja eftirfarandi skrefum.
<ol>
<li><a href="../../dev-itpro/migration-upgrade/download-hotfix-lcs.md">Sæktu lýsigagnabráðabótina á Microsoft Dynamics Lifecycle Services (LCS)</a>.</li>
<li><a href="../../dev-itpro/migration-upgrade/install-metadata-hotfix-package.md">Setja upp bráðabót lýsigagna</a>.</li>
<li><a href="../../dev-itpro/deployment/create-apply-deployable-package.md">Stofna virkjanlegan pakka</a> sem inniheldur <strong>ApplicationSuite</strong> og <strong>ProjectMobile</strong> virðislíkön og hlaða svo upp virkjanlegum pakka í LCS.</li>
<li><a href="../../dev-itpro/deployment/apply-deployable-package-system.md">Notaðu virkjanlega pakkann</a>.</li>

</ol></td>
</tr>
<tr class="even">
<td>Gefa út fartækjavinnusvæðið <strong>Vinnustundafærsla verks</strong>.</td>
<td>Kerfisstjóri</td>
<td>Sjáið <a href="../../dev-itpro/mobile-apps/publish-mobile-workspace.md">Fartækjavinnusvæði birt</a>.</td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-mobile-app"></a>Sæktu og settu upp fartækjaforritið

Sæktu og settu upp fartækjaforritið Dynamics 365 for Unified Operations:

-   [Fyrir Android síma](https://go.microsoft.com/fwlink/?linkid=850662)
-   [Fyrir iPhone síma](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a>Innskráning í fartækjaforritið
1.  Ræstu forritið í fartækinu þínu.
2.  Færðu inn vefslóð þína fyrir Dynamics 365.
3.  Í fyrsta sinn sem þú skráir þig inn, er beðið um notandanafn og aðgangsorð þitt. Færðu inn skilríki
4.  Eftir að þú hefur skráð þig inn, birtast tiltæk vinnusvæði fyrir fyrirtækið. Athugið að ef kerfisstjóri gefur út nýtt vinnusvæði síðar, verður að endurræsa listann yfir fartækjavinnusvæði.

[![Togið upp til að uppfæra](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)

## <a name="enter-time-by-using-the-project-time-entry-mobile-workspace"></a>Færið inn tíma með því að nota í fartækjavinnusvæðið Vinnustundafærsla verks
1.  Í farsímanum velurðu vinnusvæðið **Vinnustundafærsla verks**.
2.  Veljið **Vinnustundafærsla**. Dagatalsdagsetningar fyrir gildandi viku eru sýndar.
3.  Fyrir valda dagsetningu skal velja **Aðgerðir** &gt; **Ný færsla**.
4.  Færið inn fjölda klukkustunda.
5.  Veljið verkið fyrir vinnustundafærsluna. Listi sýnir verkin sem er hlaðið í forritið til notkunar utan nets. 50 atriðum er hlaðið sjálfgefið en þeirri tölu má breyta. Frekari upplýsingar má fá hér: [Fartækjaverkvangur](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md).
6.  Veldu **Leit** ef verkið er ekki á listanum. Leita eftir nafni eða skipta yfir í leit til að leita eftir nafni eða viðskiptavini.
7.  Veljið tegund. Listi sýnir flokkana sem er hlaðið í forritið til notkunar utan nets. 50 atriðum er hlaðið sjálfgefið en þeirri tölu má breyta. Frekari upplýsingar má fá hér: [Fartækjaverkvangur](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md).
8.  Veldu **Leit** ef flokkurinn er ekki á listanum. Leita eftir tegund eða skipta til að leita að nafni tegundar.
9.  Velja verkþátt. Listi sýnir aðgerðirnar sem er hlaðið í forritið til notkunar utan nets. 50 atriðum er hlaðið sjálfgefið en þeirri tölu má breyta. Frekari upplýsingar má fá hér: [Fartækjaverkvangur](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md).
10. Veldu **Leit** ef aðgerðin er ekki á listanum. Leita eftir verkþáttarnúmer eða skipta í að leita eftir tilgangi.

11. Velja línueiginleika.
12. Valfrjálst: Færðu inn innri eða ytri athugasemdir.
13. Velja **Ekkert**.

