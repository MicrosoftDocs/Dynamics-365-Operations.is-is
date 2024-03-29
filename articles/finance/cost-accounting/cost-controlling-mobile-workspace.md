---
title: Fartækjavinnusvæði kostnaðarstýringar
description: Þessi grein veitir upplýsingar um fartækjavinnusvæðið Kostnaðarstýring. Þetta vinnusvæði gerir kleift kostnaðarstaðar stjórnendur að skoða upplýsingar um kostnað vinnustöðvar afköst hvar og hvenær sem er.
author: AndersGirke
ms.date: 05/24/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CAMMobileCostObjectOverviewDetailsCurrentPeriod, CAMMobileCostObjectList, CAMMobileCostObjectOverviewDetailsPreviousPeriod, CAMMobileCostObjectOverview, CAMMobileCostObjectOverviewDetailsYearToDate, CAMMobileCostControlWorkspaceConfiguration
audience: Application User
ms.reviewer: twheeloc
ms.custom: 267114
ms.assetid: 612f2988-b2b9-420d-9825-40b99dc0e204
ms.search.region: global
ms.author: aevengir
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: 2d6d3fdcc0b0387a92f138b0ba7cf537f473b91a
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/29/2022
ms.locfileid: "9069564"
---
# <a name="cost-controlling-mobile-workspace"></a>Fartækjavinnusvæði kostnaðarstýringar

[!include [banner](../includes/banner.md)]
[!include [mobile app deprecation](../../fin-ops-core/dev-itpro/includes/mobile-app-deprecation-banner.md)]

Þessi grein veitir upplýsingar um fartækjavinnusvæðið **Kostnaðarstýring**. Þetta vinnusvæði gerir kleift kostnaðarstaðar stjórnendur að skoða upplýsingar um kostnað vinnustöðvar afköst hvar og hvenær sem er.

Þessu fartækjavinnusvæði er ætlað til að nota með farsímaforriti fjármála- og reksturs (Dynamics 365) .

## <a name="overview"></a>Yfirlit
Fartækjavinnusvæði **kostnaðarstýringar** veitir skjótt yfirlit yfir núgildandi afköst kostnaðarstaðar með samanburði á raunverulegum kostnaði og kostnaði fjárhagsáætlunar. Hægt er að kafa niður í stöðu stakra kostnaðareininga.

Til dæmis er starfsmaður fær boð um að koma á erlendar ráðstefna, en fyrirtæki verða að borga öll ferðakostnaður. Starfsmaðurinn spyr stjórnanda sinn hvort þeir geti mætt á ráðstefnuna. Stjórnandinn opnar fartækjavinnusvæði **kostnaðarstýringar** í farsímanum sínum til að sjá hvort að til sé fjárhagsáætlun fyrir því að starfsmaðurinn fari á ráðstefnuna.

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
    
    [![Spjald fyrir kostnaðareiningu.](./media/Cost-controlling.png)](./media/Cost-controlling.png)

## <a name="prerequisites"></a>Forkröfur
Skilyrðin eru breytileg, byggt á útgáfu Microsoft Dynamics 365 sem hefur verið sett upp fyrir fyrirtækið þitt.

### <a name="prerequisites-if-you-use-microsoft-dynamics-365-finance"></a>Skilyrði ef þú notar Microsoft Dynamics 365 Finance
Ef Finance hefur verið innleitt í fyrirtækinu verður kerfisstjóri að birta fartækjavinnusvæðið **Kostnaðarstýring**. Leiðbeiningar er að finna í [Fartækjavinnusvæði birt](../../fin-ops-core/dev-itpro/mobile-apps/publish-mobile-workspace.md).

### <a name="prerequisites-if-you-use-version-1611-with-platform-update-3-or-later"></a>Skilyrði ef þú notar útgáfu 1611 með verkvangsuppfærslu 3 eða nýrri
Ef útgáfa 1611 með verkvangsuppfærslu 3 eða síðar hefur verið sett upp fyrir fyrirtækið þitt, verður kerfisstjórinn að ljúka eftirfarandi skilyrðum.

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
<li><a href="/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/download-hotfix-lcs">Sækja bráðabót lýsigagna frá Microsoft Dynamics Lifecycle Services (LCS)</a>.</li>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/install-metadata-hotfix-package">Setja upp bráðabót lýsigagna</a>.</li>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/deployment/create-apply-deployable-package">Stofna virkjanlegan pakka</a> sem inniheldur <strong>SCMMobile</strong> líkanið og hlaða síðan virkjanlega pakkann í LCS.</li>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/deployment/apply-deployable-package-system">Notaðu virkjanlega pakkann</a>.</li>

</ol></td>
</tr>
<tr class="even">
<td>Gefðu út fartækjavinnusvæðið <strong>Kostnaðarstýring</strong>.</td>
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

[![Toga upp til að uppfæra.](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)

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



[!INCLUDE[footer-include](../../includes/footer-banner.md)]

