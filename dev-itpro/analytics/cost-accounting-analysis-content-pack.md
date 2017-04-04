---
title: "Kostnaðarbókhald analysis Power BI-efni"
description: "Þetta efnisatriði lýsir því hvað er tekin með í kostnaðarbókhaldi analysis Power BI efni. Það útskýrt hvernig á að ná í skýrslur Power BI og veitir upplýsingar um gagnalíkan og einingar sem voru notaðir til að byggja efni."
author: YuyuScheller
manager: AnnBe
ms.date: 2017-04-04
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: Operations
ms.custom: 270274
ms.assetid: b74549df-35d5-4f2f-b3c7-405b0d38ea78
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 388b6398488e6f316c1ec07a00182e81c1dc8d08
ms.openlocfilehash: 50e7bd92ee693f59fd013226aee22bd1a54c81e2
ms.lasthandoff: 03/31/2017


---

# <a name="cost-accounting-analysis-power-bi-content"></a>Kostnaðarbókhald analysis Power BI-efni

Þetta efnisatriði lýsir því hvað er tekin með í kostnaðarbókhaldi analysis Power BI efni. Það útskýrt hvernig á að ná í skýrslur Power BI og veitir upplýsingar um gagnalíkan og einingar sem voru notaðir til að byggja efni.

<a name="overview"></a>Yfirlit
--------

Í **kostnaðarbókhald analysis** Microsoft Power BI efni er ætluð fyrir textafyrirsögn sem er ábyrgur fyrir framkvæmd kostnaðarstýringu fyrirtækis eða að kostnaður svo hægt sé. Það felur í sér lykill mælikvörðum kostnaðar, magni línuupphæðar samræmi og kostnaðarhlutfall raunverulegur kostnaður er kostnaður fjárhagsáætlunar og kostnaður sveigjanlegrar áætlunar. Það notar færslugögn úr kostnaðarbókhald í Microsoft Dynamics 365 aðgerða og veitir yfirlit kostnaðar steypa saman fyrir öll fyrirtæki í eina skýrslugjaldmiðill. Stjórnendur hægt er að sía gögn af hlutum kostnaðar til að framkvæma kostnaðarstýringu þeirra skipulagseininga, jafnvel þótt fyrirtækið getur haft nokkrar lögaðila. Þar sem **kostnaðarbókhald analysis** Power BI efni merkir þær frávik milli raunkostnað og áætlaðan kostnað, stjórnendur geta vita jákvætt og neikvætt leitni þeirra eininga aðgerðar. Stjórnendur geta kafað niður að kostnaður einingarinnar stigveldi eða stakar einingar til að fá nákvæmar insight í hvernig frávik kostnaðar orðið, og svo bregðast virkar. Í **kostnaðarbókhald analysis** Power BI innihald let's kostnaður bókhaldarar greina kostnað flæði gegnum hlutir kostnaðar fyrir allt fyrirtækið. Sjá frekari upplýsingar um kostnaðarbókhald, [heimasíða kostnaðarbókhald](/dynamics365/operations/financials/cost-accounting/cost-accounting-home-page.md). Skilgreina aðgang á færslustigi í kostnaðarbókhaldi og hvernig sameinaðar með öryggi á línustigi í Power BI, má veita öllum kostnaðar hlut eiganda aðgang að í **kostnaðarbókhald analysis** Power BI efni. Öll gögnin í sjóngervingum sem verða svo síaðar byggt á aðgangsstig sem er stýrt í kostnaðarbókhaldi. Sjá frekari upplýsingar um aðgang á færslustigi og línu á færslustigi, [Setja upp öryggisbúnað fyrir kostnaðarbókhalds efni fyrir Power BI](setup-security-cost-accounting-content-pack.md).

## <a name="accessing-the-power-bi-content"></a>Fara í hugbúnaðarhlutartréð innihald Power BI
Hægt er að finna í **kostnaðarbókhald analysis** Power BI efni í eignir safn Samnýttum í Microsoft Dynamics Lifecycle Services (LCS). Nánari upplýsingar um hvernig á að sækja efni og að tengjast við Dynamics 365 fyrir Aðgerðir í [Power BI efni í LCS frá Microsoft og for your viðskiptaaðila](power-bi-content-microsoft-partners.md). **Athugasemd:** KB4011327 ** ** er forskilyrði fyrir að í **kostnaðarbókhald analysis** Power BI efni.  Eftir að innskráning á Lifecycle Services, er hægt að opna KB hér: <https://fix.lcs.dynamics.com/issue/results/?q=kb4011327>.

## <a name="metrics-that-are-included-in-the-power-bi-content"></a>Einingar sem eru hafðar með í efni Power BI
Innihald inniheldur safn af skýrslusíðum. Hverri síðu samanstendur af safni einingar sem eru visualized sem gröf reitir og töflur. Eftirfarandi tafla veitir yfirlit yfir sjóngervingum í á **kostnaðarbókhald analysis** Power BI efni.

| Skýrslan síðu                      | Graf                                                                                                                         | Reitur                                          |
|----------------------------------|-------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| Kostnaðarstýring eftir fjárhagstímabili    | Raunverulegur kostnaður og kostnaður Fjárhagsáætlunar með Kostnað stigveldisstig einingu                                                                   | Raunverulegur kostnaður miðað við Áætlun kostnaðar                    |
|                                  | Fjárhagsfrávik með Kostnað stigveldisstig einingu                                                                               | Raunverulegur kostnaður miðað við gengi Fjárhagsáætlunar kostnaður taxta          |
|                                  | 10 efstu fjárhagsfrávik í prósentum af kostnaðareiningu                                                                          | Magni línuupphæðar magni línuupphæðar samræmi raun samanb. v. Áætlun samræmi          |
| Kostnaðarstýring eftir Ári     | Raunverulegur kostnaður og kostnaður í Fjárhagsáætlun eftir Tímabilum fyrir Almanaksár                                                                           | Raunverulegur kostnaður miðað við Áætlun kostnaðar                    |
|                                  | Fjárhagsfrávik eftir Tímabilum fyrir Almanaksár                                                                                       | Raunverulegur kostnaður miðað við gengi Fjárhagsáætlunar kostnaður taxta          |
|                                  | 10 efstu fjárhagsfrávik í prósentum af kostnaðareiningu                                                                          | Magni línuupphæðar magni línuupphæðar samræmi raun samanb. v. Áætlun samræmi          |
| Kostnaðarhlutfalls eftir fjárhagsár         | Raunverulegt kostnaðarhlutfall með hegðun Kostnaðar                                                                                             | Raunverulegur kostnaður miðað við gengi Fjárhagsáætlunar kostnaður taxta          |
|                                  | Raunverulegt kostnaðarhlutfall Áætlunar kostnaðarfrávik taxta, Fjárhagsáætlunar prósentu taxta og kostnaðarhlutfall Áætlunar með Kostnað stigveldisstig einingu | Magni línuupphæðar magni línuupphæðar samræmi raun samanb. v. Áætlun samræmi          |
|                                  | Fjárhagsfrávik með Kostnað stigveldisstig einingu                                                                               |                                               |
|                                  | 10 efstu fjárhagsfrávik í prósentum af kostnaðareiningu                                                                          |                                               |
| Sveigjanlegrar áætlunar eftir fjárhagstímabili | Raunverulegur kostnaður, Fjárhagsáætlunar og Sveigjanlega áætlun kostnaðarverðs með Kostnað stigveldisstig einingu                                             | Magni línuupphæðar magni línuupphæðar samræmi raun samanb. v. Áætlun samræmi          |
|                                  | Fjárhagsfrávik og frávikið sveigjanlegar áætlanir með Kostnað stigveldisstig einingu                                                  | Raunverulegur kostnaður miðað við Sveigjanlega áætlun kostnaðar           |
|                                  | Raunverulegur kostnaður áætlunar og Sveigjanlegur kostnaður með hegðun og Kostnaðarbreytingum stigveldisstig einingu                                  | Taxti samanb. v. Sveigjanlega áætlun kostnaðar raunkostnaðarhlutfall |
| Kostnaðaryfirlit eftir fjárhagstímabili  | Raunverulegur kostnaður með stigveldisstig einingu og Kostnaðarbreytingum stak víddarheiti hlut                                             |                                               |
|                                  | Raunverulegur kostnaður eftir Kostnaður hlut vídd stak heiti og Kostnaður nafn staks vídd einingar                                       |                                               |

## <a name="understanding-the-data-model-and-entities"></a>Skilja gagnalíkan og einingar
Dynamics 365 fyrir Aðgerðir sem er notuð til að fylla á skýrslusíðum á **kostnaðarbókhald analysis** Power BI efni. Þessum gögnum er birtur sem uppsöfnuðum mælingum sem stig eru í versluninni Einingar sem er Microsoft SQL-gagnagrunnur sem er fínstillt fyrir greiningu. Nánari upplýsingar, sjá [Yfirlit Power BI samþættingu við verslun Einingar](power-bi-integration-entity-store.md). Eftirfarandi lykli uppsafnaðar mælingar eru notaðar sem grunnur fyrir efni.

| Eining                  | Lykill uppsafnaða mælingu | Gagnagjafi fyrir Dynamics 365 fyrir Aðgerðir | Svæði     | lýsing                                   |
|-------------------------|---------------------------|---------------------------------------------|-----------|-----------------------------------------------|
| Færslur kostnaðarbókhalds | SUM(Amount)               | CAMDATAAggregatedCostEntry                  | Upphæð    | Upphæð í gjaldmiðli fyrir fjárhag kostnaðarbókhalds |
| Tölfræðilegar færslur     | SUM(Magnitude)            | CAMDATAAggregatedStatisctialEntry           | Mæligildi |                                               |

Eftirfarandi tafla sýnir hvernig uppsafnaðar mælingar lykli eru notaðar til að stofna reiknaðar mælieiningar í gagnasafni sem efni.

| Mæla                                       | Hvernig mælieiningu sem er reiknað                                                                                          |
|-----------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| Raunkostnaður                                   | REIKNA ('Kostnaður bókhaldsfærslur'\[Mælieiningu\], 'Færsla útgáfur'\[ISSOURCEVERSIONBUDGET\_GILDI\] = 0)            |
| Áætlaður kostnaður                                   | REIKNA ('Kostnaður bókhaldsfærslur'\[Mælieiningu\], 'Færsla útgáfur'\[ISSOURCEVERSIONBUDGET\_GILDI\] = 1)            |
| Frávik fjárhagsáætlunar                          | \[Kostnaður fjárhagsáætlunar\] - \[raunkostnaður\]                                                                                      |
| Frávikaprósenta fjárhagsáætlunar                    | EF (\[kostnaður Fjárhagsáætlunar\] = 0, blank(), \[fjárhagsfrávik\] / \[kostnaður Fjárhagsáætlunar\])                                                |
| Magni línuupphæðar samræmi raunverulegu                              | REIKNA ('Tölfræðilega færslum'\[FullMagnitude\], 'Færsla útgáfur'\[ISSOURCEVERSIONBUDGET\_GILDI\] = 0)          |
| Magni línuupphæðar samræmi fjárhagsáætlunar                              | REIKNA (\[FullMagnitude\], 'Færsla útgáfur'\[ISSOURCEVERSIONBUDGET\_GILDI\] = 1)                               |
| Fjárhagsfrávik talnagagna                   | \[Magni línuupphæðar samræmi fjárhagsáætlunar\] - \[Raunverulegt magni línuupphæðar í samræmi.\]                                                                            |
| Frávikaprósenta tölfræðilega fjárhagsáætlunar        | EF (\[Fjárhagsáætlunar magni línuupphæðar í samræmi\] = 0, blank(), \[Tölfræðilega fjárhagsfrávik\] / \[Fjárhagsáætlunar magni línuupphæðar í samræmi\])                          |
| Raunverulegt kostnaðarhlutfall                              | EF (\[Raunverulegt magni línuupphæðar í samræmi\] = 0 BLANK(), \[raunkostnaður\] / \[Raunverulegt magni línuupphæðar í samræmi\])                                          |
| Kostnaðarhlutfall áætlunar                              | EF (\[Fjárhagsáætlunar magni línuupphæðar í samræmi\] = 0 BLANK(), \[kostnaður Fjárhagsáætlunar\] / \[Fjárhagsáætlunar magni línuupphæðar í samræmi\])                                          |
| Áætlaður kostnaður gengi frávika                     | \[Kostnaðarhlutfall áætlunar\] - \[Raunverulegt kostnaðarhlutfall\]                                                                            |
| Frávikaprósenta gengi fjárhagsáætlunar          | EF (\[kostnaður Fjárhagsáætlunar\] = 0, blank(), \[kostnaðarfrávik gengi Fjárhagsáætlunar\] / \[kostnaðarhlutfall Áætlunar\])                                 |
| Föst áætlun kostnaðar                             | REIKNA (\[kostnaður Fjárhagsáætlunar\], "Kostnaður bókhaldsfærslur"\[COSTBEHAVIOR\] = 1)                                              |
| Breytileg áætlun kostnaðar                          | REIKNA (\[kostnaður Fjárhagsáætlunar\], "Bókhaldsfærslur Kostnaður"\[COSTBEHAVIOR\] = 2)                                              |
| Sveigjanlegar áætlanir fastan kostnað                    | \[Föst áætlun kostnaðar\]                                                                                                  |
| Breytileg sveigjanlega áætlun kostnaðar                 | EF (\[Fjárhagsáætlunar magni línuupphæðar í samræmi\] = 0, BLANK(), (\[Breytilegrar áætlunar\] / \[Fjárhagsáætlunar magni línuupphæðar í samræmi\]) \*\[Raunverulegt magni línuupphæðar í samræmi\])       |
| Kostnaður sveigjanlegrar áætlunar                          | \[Fastur kostnaður sveigjanlegrar áætlunar\] + \[Breytileg sveigjanlega áætlun kostnaðar\]                                                     |
| Frávik sveigjanlega áætlun                      | \[Kostnaður sveigjanlegrar áætlunar\] - \[raunkostnaður\]                                                                             |
| Frávikaprósenta sveigjanlega áætlun           | EF (\[kostnaður Sveigjanlegrar áætlunar\] = 0, BLANK(), \[Sveigjanlega fjárhagsfrávik\] / \[kostnaður Sveigjanlegrar áætlunar\])                     |
| Kostnaður sveigjanlegrar áætlunar taxta                     | EF (\[Raunverulegt magni línuupphæðar í samræmi\] = 0, BLANK(), \[kostnaður Sveigjanlegrar áætlunar\] / \[Raunverulegt magni línuupphæðar í samræmi\])                                 |
| Kostnaður sveigjanlegrar áætlunar gengi frávika            | \[Kostnaðarhlutfall sveigjanlegrar áætlunar\] - \[Raunverulegt kostnaðarhlutfall\]                                                                   |
| Frávikaprósenta taxta kostnaður sveigjanlegrar áætlunar | EF (\[kostnaðarhlutfall Sveigjanlegrar áætlunar\] = 0, BLANK(), \[kostnaður Sveigjanlegrar áætlunar gengi frávika\] / \[kostnaðarhlutfall Sveigjanlegrar áætlunar\]) |

Eftirfarandi lykill eru notaðar þær víddir sem síur til að sneiða uppsafnaðar mælingar til að ná uppskiptingin hærri og veita hærra insights greiningar.

| Eining                             | Dæmi um eigindir                                                                                               |
|------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| Fjárhagir kostnaðarbókhalds            | Fjárhagur kostnaðarbókhalds                                                                                               |
| Stýrieiningar kostnaðar                 | Heiti stýrieiningar kostnaðar                                                                                               |
| Víddir kostnaðareiningar            | Kostnaður einingar vídd nafn, Kostnaður nafn staks vídd einingar, Kostnaður lýsingu stak vídd einingar          |
| Víddir kostnaðarhluta             | Kostnaður heiti hlutar vídd, Kostnaður hlut vídd stak heiti, Kostnaður hlut vídd stak lýsingu              |
| Tölfræðilegar víddir             | Tölfræðilega víddarheiti, nafn staks Tölfræðilega vídd, lýsingu stak Tölfræðilega vídd              |
| Víddastigveldi kostnaðar hlut  | Kostnaður hlut stigveldisheiti vídd, Kostnaður hlut vídd stigveldisstig, Kostnaður víddastigveldistrénu hlut    |
| Víddastigveldi kostnaðar einingu | Kostnaður á einingu stigveldisheiti vídd, Kostnað á einingu vídd stigveldisstig, eining víddastigveldistrénu Kostnaðar |
| Tölfræðileg víddastigveldi  | Stigveldisheiti tölfræðilegum vídd, stigveldisstig Tölfræðilegum vídd, Tölfræðilegum víddastigveldistrénu    |
| Færsluútgáfur               | Útgáfunafn                                                                                                         |
| Fjárhagsdagatöl                   | Dagatal lýsing Dagatals                                                                                       |
| Fjárhagsár                       | Almanaksár                                                                                                        |
| Fjárhagstímabil                     | Tímabil fyrir almanaksár                                                                                                 |

## <a name="additional-resources"></a>Frekari upplýsingar
Hér eru gagnlegir tenglar sem tengjast einingar og að búa til Power BI-efni:

-   [Gagnaeiningar](..\data-entities\data-entities.md)
-   [Stofnun efnispakka fyrirtækis ](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   [Gera gagnalíkön með því að nota Power BI](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [Bæta Power BI-reitum við vinnusvæði](configure-power-bi-integration.md)
-   [Setja upp öryggi kostnaðarbókhald efni fyrir Power BI](setup-security-cost-accounting-content-pack.md)


