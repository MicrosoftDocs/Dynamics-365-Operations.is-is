---
title: "Fartækjavinnusvæði kostnaðarstýringar fyrir forritið Microsoft Dynamics 365 for Operations"
description: "Með fartækjavinnusvæði kostnaðarstýringar geta stjórnendur kostnaðarstaðar séð afkomu kostnaðarstaðar hvenær sem er og hvar sem er."
author: YuyuScheller
manager: AnnBe
ms.date: 2017-01-12 16 - 53 - 04
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 267114
ms.assetid: 84740472-494f-444c-9b74-f83b7342fd25
ms.search.region: global
ms.author: yuyus
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: c8c96dc9705688308dd4a5c720700ddc17657d75
ms.openlocfilehash: 8136efb1d2669c39fcc0f80b60e80ecae983d5d8
ms.lasthandoff: 03/31/2017


---

# <a name="cost-controlling-mobile-workspace-for-microsoft-dynamics-365-for-operations-app"></a>Fartækjavinnusvæði kostnaðarstýringar fyrir forritið Microsoft Dynamics 365 for Operations

Með fartækjavinnusvæði kostnaðarstýringar geta stjórnendur kostnaðarstaðar séð afkomu kostnaðarstaðar hvenær sem er og hvar sem er. 

<a name="prerequisites"></a>Forkröfur
-------------

| Skilyrði                                                         | lýsing                                                                                                                                                                   |
|----------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Lesa um Microsoft Dynamics 365 for Operations verkvang | [Microsoft Dynamics 365 for Operations verkvangur](/dynamics365/operations/dev-itpro/mobile-apps/mobile-platform)                                                              |
| Dynamics 365 for Operations                                          | Vertu viss um að þú sért að nota umhverfi sem er með Microsoft Dynamics 365 for Operations útgáfu 1611 og uppfærslu verkvangs Microsoft Dynamics for Operations 3 (nóvember 2016). |
| Bráðabót KB 3215650                                                    | Setja upp bráðabót til að virkja vinnusvæðin sem veitt eru í Microsoft Dynamics 365 for Operations.                                                                       |
| Lýsingarlína fartækis með forritið Dynamics 365 for Operations uppsett | Sækja forritið Dynamics 365 for Operations úr forritaverslun fartækis.                                                                                                      |

## <a name="introduction"></a>Inngangur
Fartækjavinnusvæði kostnaðarstýringar veitir skjótt yfirlit yfir  núgildandi afkomu kostnaðarstaðar með samanburði á raunverulegum kostnaði og kostnaði fjárhagsáætlunar. Hægt er að kafa niður í stöður stakra kostnaðareininga.

### <a name="example"></a>Dæmi

Starfsmaður fær boð á alþjóðlega ráðstefnu. Fyrirtækið verður að greiða allan ferðakostnað. Starfsmaðurinn spyr yfirmann sinn hvort að hann geti farið á ráðstefnuna. Stjórnandinn opnar snöggvast fartækjavinnusvæði kostnaðarstýringar í farsímanum sínum til að sjá hvort að til sé fjárhagsáætlun fyrir því að starfsmaðurinn fari á ráðstefnuna.

### <a name="data-security"></a>Öryggi gagna

Gögnin í vinnusvæði kostnaðarstýringar eru tryggð með notandaskilríkjum. Stjórnandi kostnaðarstaðar hefur aðeins leyfi til að skoða gögn fyrir sinn eigin kostnaðarstað. Öryggi aðgangsstigs er stjórnað innan einingarinnar Kostnaðarbókhald. Kostnaðarbókarar skilgreina grunnstillingar fartækjavinnusvæðis kostnaðarstýringar í einingunni Kostnaðarbókhald. Þegar vinnusvæðið hefur verið gefið út í forritinu Microsoft Dynamics 365 for Operations er það tiltækt í fartækjaforriti Dynamics 365 for Operations. Þetta tryggir að allir stjórnendur kostnaðarstaða í fyrirtækinu skoði gögn á sama sniði.

### <a name="actions-views-and-links"></a>Aðgerðir, yfirlit og tenglar

Fartækjavinnusvæði kostnaðarstýringar fyrir forritið Dynamics 365 for Operations veitir eftirfarandi aðgerðir, yfirlit og tengla:

-   Aðgerðir 
    -   Veldu **Skilgreiningar** til að taka til útlit.
    -   Veldu **Kostnaðarhlutur** til að taka til kostnaðarstað þar sem þú vilt sía gögn. **athugasemd:** Listinn er birtur samkvæmt aðgangnum sem var veittur í einingunni Kostnaðarbókhald.

<!-- -->

-   Á grunni þess sem er valið undir **Aðgerðir** og þess sem er skilgreint í einingunni Kostnaðarbókhald er hægt að skoða eftirfarandi upplýsingar í Kort. Athugaðu að upphæðin er birt á sama sniði: Raun-, Fjárhagsáætlun, Frávik, og Frávik %. 
    -   Raunverulegt samanb. v. áætlun (núgildandi tímabil)
    -   Raunverulegt samanb. v. endurskoðaða fjárhagsáætlun (núgildandi tímabil)
    -   Raunverulegt samanb. v. áætlun (fyrra tímabil)
    -   Raunverulegt samanb. v. endurskoðaða fjárhagsáætlun (fyrra tímabil)
    -   Raunverulegt samanb. v. áætlun (það sem af er ári)
    -   Raunverulegt samanb. v. endurskoðaða fjárhagsáætlun (það sem af er ári)

<!-- -->

-   Tenglar
    -   Sundurliðun fyrir núverandi tímabil.
    -   Sundurliðun fyrir fyrra tímabil.
    -   Sundurliðun fyrir það sem af er árinu.

Þegar þú velur einn af tenglunum er kort á kostnaðareiningu birt. Upphæð á kortunum er birt á eftirfarandi sniði: Raun-, Fjárhagsáætlun, Frávik, og Frávik %, Endurskoðuð fjárhagsáætlun, Frávik endurskoðaðrar fjárhagsáætlunar og Frávik endurskoðaðrar fjárhagsáætlunar %.  [![cost-controlling](./media/cost-controlling.png)](./media/cost-controlling.png)

## <a name="get-started"></a>Hefjast handa
Fylgið eftirfarandi skrefum til að hefja notkun á kostnaðarstýringu í farsímaforriti í fartæki fyrirtækisins.

1.  Sæktu forritið Microsoft Dynamics 365 for Operations úr forritaverslun farsímans og settu það upp.
2.  Ræstu forritið í snjallsímanum.
3.  Færðu inn vefslóð þína fyrir Dynamics 365.
4.  Skráðu fyrirtækið sem á að skrá sig inn á . Til dæmis: Færið inn **USMF**.
5.  Fyrsta skipti‘ sem þú skráir þig inn verðurðu beðin um notandanafn og aðgangsorð fyrir þinn Microsoft Dynamics 365 for Operations reikning. Færðu inn skilríki Eftir að þú skrá inn, sérðu tiltækt vinnusvæði fyrir Þitt fyrirtæki.

Til að skoða vinnusvæði í farsímaforritinu verður fyrst að gefa út æskileg vinnusvæði í forritið Dynamics 365 for Operations.

1.  Ræstu Dynamics 365 for Operations.
2.  Opnaðu **Kerfisstjórnun** &gt; **Uppsetning** &gt; **kerfisfæribreytur**.
3.  Veldu **Stjórna fartækjaforriti**.
4.  Velja vinnusvæðið **Kostnaðarstýring** til að birta í verkvangi farsíma.
5.  Veldu **Birta vinnusvæði**.
6.  Endurhlaða Þitt tæki til að sjá útgefin vinnusvæði.

## <a name="view-the-performance-of-your-cost-center"></a>Skoða vinnsluhraða kostnaðarstaðar
1.  Í farsímanum velurðu vinnusvæðið **Kostnaðarstýring**.
2.  Veldu **Stjórnborð kostnaðarhlutar**.
3.  Smellt er á **Aðgerðir**.
4.  Smellið á **Velja grunnstilling** til að velja útlit kostnaðarstýringar.
5.  Smelltu á **Lokið**.
6.  Smellt er á **Aðgerðir**.
7.  Smellt er á **Velja kostnaðarhlut** til að velja kostnaðarstað sem þú hefur fengið aðgang að.
8.  Smelltu á **Lokið**.
9.  Skoða heildarafkomu kostnaðarstaðar.
10. Smellt er á **Sundurliðun fyrir núverandi tímabil**.
11. Skoða vinnsluhraða stakra kostnaðareininga.
12. Einnig má leita að sérstökum kostnaðareiningum.



