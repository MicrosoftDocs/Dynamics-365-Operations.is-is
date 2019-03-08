---
title: Fartækjavinnusvæði kostnaðarstýringar
description: Þetta efnisatriði veitir upplýsingar um fartækjavinnusvæðið Kostnaðarstýring. Þetta vinnusvæði gerir kleift kostnaðarstaðar stjórnendur að skoða upplýsingar um kostnað vinnustöðvar afköst hvar og hvenær sem er.
author: AndersGirke
manager: AnnBe
ms.date: 12/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 267114
ms.assetid: 612f2988-b2b9-420d-9825-40b99dc0e204
ms.search.region: global
ms.author: aevengir
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: b6cdb69f32de2118e685c149605d50b78105c098
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/29/2019
ms.locfileid: "317569"
---
# <a name="cost-controlling-mobile-workspace"></a>Fartækjavinnusvæði kostnaðarstýringar

[!include [banner](../includes/banner.md)]

Þetta efnisatriði veitir upplýsingar um fartækjavinnusvæðið **Kostnaðarstýring**. Þetta vinnusvæði gerir kleift kostnaðarstaðar stjórnendur að skoða upplýsingar um kostnað vinnustöðvar afköst hvar og hvenær sem er.

Þetta fartækjavinnusvæði er ætlað til að nota með Microsoft Dynamics 365 fyrir farsímaforritið Unified Operations Mobile.

## <a name="overview"></a>Yfirlit
Fartækjavinnusvæði **kostnaðarstýringar** veitir skjótt yfirlit yfir núgildandi afköst kostnaðarstaðar með samanburði á raunverulegum kostnaði og kostnaði fjárhagsáætlunar. Hægt er að kafa niður í stöðu stakra kostnaðareininga.

Til dæmis er starfsmaður fær boð um að koma á erlendar ráðstefna, en fyrirtæki verða að borga öll ferðakostnaður. Starfsmaðurinn spyr yfirmann sinn hvort að hann geti farið á ráðstefnuna. Stjórnandinn opnar fartækjavinnusvæði **kostnaðarstýringar** í farsímanum sínum til að sjá hvort að til sé fjárhagsáætlun fyrir því að starfsmaðurinn fari á ráðstefnuna.

### <a name="data-security"></a>Öryggi gagna
Gögnin í fartækjavinnusvæði **Kostnaðarstýring** eru tryggð með notandaskilríkjum. Stjórnendur kostnaðarstaðar hafa aðeins leyfi til að skoða gögn fyrir eigin kostnaðarstað. Aðgangsstigs örygginu er stjórnað innan einingarinnar **Kostnaðarbókhald**.

Kostnaðarbókarar skilgreina grunnstillingar fartækjavinnusvæðis **Kostnaðarstýringar** í einingunni **Kostnaðarbókhald**. Þegar vinnusvæðið hefur verið sett í fartækjaforritið er það tiltækt í forritinu. Þannig geta allir stjórnendur kostnaðarstaða í fyrirtækinu skoðað gögn á sama sniði.

### <a name="actions-views-and-links"></a>Aðgerðir, yfirlit og tenglar
Fartækjavinnusvæðið **Kostnaðarstýring** býður upp á eftirfarandi aðgerðir, yfirlit og tengla:

-   **Aðgerðir:**

    -   Notið **Velja skilgreiningu** til að velja útlit.
    -   Notið **Valin Hluturinn kostnaður** til að velja kostnaðarstaði til að sía gögnin á.
    
        > [!NOTE]
        > Þeir kostnaðarstaðir sem birtast á listanum eru háðir aðgangi sem er veittur í einingunni **Kostnaðarbókhald**.

-   **Yfirlit:** Á grundvelli aðgerða sem eru valdar og skilgreiningar í einingunni **Kostnaðarbókhald** er hægt að skoða eftirfarandi upplýsingar á spjöldunum:

    -   Raunverulegt samanb. v. fjárhagsáætlun (núgildandi tímabil)
    -   Raunverulegt samanb. v. endurskoðaða fjárhagsáætlun (núgildandi tímabil)
    -   Raunverulegt samanb. v. fjárhagsáætlun (fyrra tímabil)
    -   Raunverulegt samanb. v. endurskoðaða fjárhagsáætlun (fyrra tímabil)
    -   Raunverulegt samanb. v. fjárhagsáætlun (það sem af er ári)
    -   Raunverulegt samanb. v. endurskoðaða fjárhagsáætlun (á árinu)

    Eftirfarandi upphæðir eru sýndar á hverju spjaldi: Raunverulegar, fjárhagsáætlun, frávik og frávik %.

-   **Tenglar:**

    -   Sundurliðun fyrir núverandi tímabil
    -   Sundurliðun fyrir fyrra tímabil
    -   Sundurliðun fyrir það sem af er árinu

    Þegar tengill er valinn, spjald er sýndur fyrir hvern kostnaðarlið. Eftirfarandi upphæðir eru sýndar á spjöldunum: Raunverulegar, fjárhagsáætlun, Fjárhagsáætlunar Frávik, Fjárhagsáætlunar Frávik %, Endurskoðuð fjárhagsáætlun, Frávik endurskoðaðrar fjárhagsáætlunar og Frávik endurskoðaðrar fjárhagsáætlunar %.
    
    [![Spjald fyrir kostnaðareiningu ](./media/Cost-controlling.png)](./media/Cost-controlling.png)

## <a name="prerequisites"></a>Forkröfur
Skilyrðin eru breytileg, byggt á útgáfu Microsoft Dynamics 365 sem hefur verið sett upp fyrir fyrirtækið þitt.

### <a name="prerequisites-if-you-use-microsoft-dynamics-365-for-finance-and-operations"></a>Skilyrði ef þú notar Microsoft Dynamics 365 for Finance and Operations
Ef Microsoft Dynamics 365 for Finance and Operations hefur verið innleitt í fyrirtækinu verður kerfisstjóri að birta fartækjavinnusvæðið **Kostnaðarstýring**. Leiðbeiningar er að finna í [Fartækjavinnusvæði birt](../../dev-itpro/mobile-apps/publish-mobile-workspace.md).

### <a name="prerequisites-if-you-use-microsoft-dynamics-365-for-operations-version-1611-with-platform-update-3-or-later"></a>Skilyrði ef þú notar Microsoft Dynamics 365 for Operations útgáfu 1611 með verkvangsuppfærslu 3 eða nýrri
Ef Microsoft Dynamics 365 for Operations útgáfa 1611 með verkvangsuppfærslu 3 eða síðar hefur verið sett upp fyrir fyrirtækið þitt, verður kerfisstjórinn að ljúka eftirfarandi skilyrðum.

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

<td>KB 4013633 er X++ uppfærsla eða lýsigagnabráðabót sem inniheldur fartækjavinnusvæðið <strong>Kostnaðarstýring</strong>. Til að setja upp KB 4013633 verður kerfisstjóri að fylgja eftirfarandi skrefum.
<ol>
<li><a href="../../dev-itpro/migration-upgrade/download-hotfix-lcs.md">Sækja bráðabót lýsigagna frá Microsoft Dynamics Lifecycle Services (LCS)</a>.</li>
<li><a href="../../dev-itpro/migration-upgrade/install-metadata-hotfix-package.md">Setja upp bráðabót lýsigagna</a>.</li>
<li><a href="../../dev-itpro/deployment/create-apply-deployable-package.md">Stofna virkjanlegan pakka</a> sem inniheldur <strong>SCMMobile</strong> líkanið og hlaða síðan virkjanlega pakkann í LCS.</li>
<li><a href="../../dev-itpro/deployment/apply-deployable-package-system.md">Notaðu virkjanlega pakkann</a>.</li>

</ol></td>
</tr>
<tr class="even">
<td>Gefðu út fartækjavinnusvæðið <strong>Kostnaðarstýring</strong>.</td>
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

## <a name="view-the-performance-of-your-cost-center-by-using-the-cost-controlling-mobile-workspace"></a>Skoða árangur þinn kostnaðarstaður með því að nota Kostnaðarstýra fartækja vinnusvæði

1.  Í farsímanum velurðu vinnusvæðið **Kostnaðarstýring**.
2.  Veldu **Stjórnborð kostnaðarhlutar**.
3.  Velja **Aðgerðir**.
4.  Smellið á **Velja grunnstillingu** til að velja útlit kostnaðarstýringar.
5.  Velja **Ekkert**.
6.  Velja **Aðgerðir**.
7.  Velja **Velja kostnaðarhlut** til að velja kostnaðarstað sem þú hefur fengið aðgang að.
8.  Velja **Ekkert**.
9.  Skoða heildarafkomu kostnaðarstaðar.
10. Veljið **Upplýsingar fyrir núverandi tímabil** tengil.
11. Skoða vinnsluhraða stakra kostnaðareininga.
12. Einnig má leita að sérstökum kostnaðareiningum.

