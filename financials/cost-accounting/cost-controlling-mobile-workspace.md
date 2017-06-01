---
title: "Fartækjavinnusvæði kostnaðarstýringar"
description: "Þetta efnisatriði veitir upplýsingar um fartækjavinnusvæði kostnaðarstýringar, sem er tiltækt fyrir Microsoft Dynamics 365 fyrir Operations farsímaforritið. Þetta vinnusvæði gerir kleift kostnaðarstaðar stjórnendur að skoða upplýsingar um kostnað vinnustöðvar afköst hvar og hvenær sem er."
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
ms.custom: 267114
ms.assetid: 612f2988-b2b9-420d-9825-40b99dc0e204
ms.search.region: global
ms.author: yuyus
ms.dyn365.ops.intro: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 09383c24b0dd2ad61a836f6c8dc97f4389915772
ms.contentlocale: is-is
ms.lasthandoff: 05/25/2017


---

# <a name="cost-controlling-mobile-workspace"></a>Fartækjavinnusvæði kostnaðarstýringar

[!include[banner](../includes/banner.md)]


Þetta efnisatriði veitir upplýsingar um fartækjavinnusvæði kostnaðarstýringar, sem er tiltækt fyrir Microsoft Dynamics 365 fyrir Operations farsímaforritið. Þetta vinnusvæði gerir kleift kostnaðarstaðar stjórnendur að skoða upplýsingar um kostnað vinnustöðvar afköst hvar og hvenær sem er. 

<a name="overview-of-the-cost-controlling-mobile-workspace"></a>Yfirlit yfir fartækjavinnusvæði kostnaðarstýringar
-------------------------------------------------

Fartækjavinnusvæði **kostnaðarstýringar** veitir skjótt yfirlit yfir núgildandi afköst kostnaðarstaðar með samanburði á raunverulegum kostnaði og kostnaði fjárhagsáætlunar. Hægt er að kafa niður í stöður stakra kostnaðareininga. 

Til dæmis er starfsmaður fær boð um að koma á erlendar ráðstefna, en fyrirtæki verða að borga öll ferðakostnaður. Starfsmaðurinn spyr yfirmann sinn hvort að hann geti farið á ráðstefnuna. Stjórnandinn opnar fartækjavinnusvæði **kostnaðarstýringar** í farsímanum sínum til að sjá hvort að til sé fjárhagsáætlun fyrir því að starfsmaðurinn fari á ráðstefnuna.

### <a name="data-security"></a>Öryggi gagna

Gögnin í fartækjavinnusvæði **Kostnaðarstýring** eru tryggð með notandaskilríkjum. Stjórnendur kostnaðarstaðar hafa aðeins leyfi til að skoða gögn fyrir eigin kostnaðarstað. Aðgangsstigs örygginu er stjórnað innan einingarinnar **Kostnaðarbókhald**. 

Kostnaðarbókarar skilgreina grunnstillingar fartækjavinnusvæðis **Kostnaðarstýringar** í einingunni **Kostnaðarbókhald**. Þegar vinnusvæðið hefur verið sett í Microsoft Dynamics 365 fyrir Operations farsímaforrit, er það tiltækt í fartækjaforritinu. Þannig geta allir stjórnendur kostnaðarstaða í fyrirtækinu skoðað gögn á sama sniði.

### <a name="actions-views-and-links"></a>Aðgerðir, yfirlit og tenglar

Fartækjavinnusvæði **kostnaðarstýringar** fyrir forritið Dynamics 365 fyrir Operations býður upp á eftirfarandi aðgerðir, yfirlit og tengla:

-   **Aðgerðir:**
    -   Notið **Velja skilgreiningu** til að velja útlit.
    -   Notið **Valin Hluturinn kostnaður** til að velja kostnaðarstaði til að sía gögnin á. **Athugasemd:** kostnaðarstaðir sem birtast á listanum eru háðir aðgangi sem eru veittar í **kostnaðarbókhalds** kerfi.
-   **Skáir:** Á grunni þess sem er valið undir Aðgerðir og þess sem er skilgreint í einingunni **Kostnaðarbókhald** er hægt að skoða eftirfarandi upplýsingar á spjöldunum.
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
    
    [![Spjald fyrir kostnaðareiningu ](./media/cost-controlling.png)](./media/cost-controlling.png)

## <a name="prerequisites"></a>Frumskilyrði
Áður en hægt er að nota **kostnaðarstýring** fartækjavinnusvæði gangið úr skugga um að kerfisstjórinn hafi tryggt eftirfarandi skilyrði.

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
<td>Ef ekki er þegar Dynamics 365 for Operations starfrækt í fyrirtækinu, skal kerfisstjóri sjá <a href="/dynamics365/operations/dev-itpro/deployment/deploy-demo-environment">Deploy Microsoft Dynamics 365 fyrir Operations sýnigögn prófunarumhverfi</a>.</td>
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
<td><strong>Kostnaðarstýring</strong> fartækja vinnusvæði verður að birtast í Dynamics 365 fyrir Operations farsímaforrit.</td>
<td>Kerfisstjóri</td>
<td><ol>
<li>Opnaðu Dynamics 365 fyrir Operations í vafranum þínum.</li>
<li>Á <strong>kerfisfæribreytum</strong> síðunni, veljið <strong>Stjórna fartækja vinnusvæði</strong>.</li>
<li>Veljið <strong>Kostnaðar yfirlit yfir þjónustuhluta</strong> vinnusvæðisins.</li>
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





