---
title: Heimasíða kostnaðarstjórnunar
description: Kostnaðarstjórnun leyfir notanda að sjá um mat og bókahald á hráefnum, hálfunnum vörum, fullunnum vörum og eignum í vinnslu.
author: AndersGirke
manager: AnnBe
ms.date: 04/25/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CostAdminWorkspace, CostAnalysisWorkspace
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: dd51fa667fd48b7bab64c3566b616631c6f9bcd1
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/30/2019
ms.locfileid: "2249633"
---
# <a name="cost-management-home-page"></a>Heimasíða kostnaðarstjórnunar

[!include [banner](../includes/banner.md)]

[Kostnaðarstjórnun (myndband)](https://www.youtube.com/watch?v=vXzlC-mOBcg&feature=youtu.be) leyfir notanda að vinna með mat og bókhald á hráefnum, hálfunnum vörum, fullunnum vörum og eignum í vinnslu. Þetta er skilgreiningar-, stjórnunar- og skýrsluferli [Birgðabókhalds](cost-object.md) og [Bókhalds framleiðslu](bom-calculations.md).

Hægt er að skilgreina kostnaðarreglur fyrir eftirfarandi svæði: 
-  [Fyrirframákveðinn kostnaður](costing-versions.md)
-  [Birgðabókhald](cost-object.md)
-  [Bókhald framleiðslu](bom-calculations.md)
-  [Óbeint kostnaðarbókhald](costing-sheets.md)
-  [Fjárhagssamþætting](production-order-cost-analysis.md)

Sem dæmi er hægt að skilgreina hvaða birgðamatsaðferð, líkt og [FIFO](fifo-physical-value-marking.md), [Vegið meðaltal](weighted-average-physical-value-marking.md), [Staðalkostnaður](prerequisites-standard-costs.md) eða [Hlaupandi meðaltal](moving-average.md), eigi að nota á afurðir í [Vörulíkanaflokki](../inventory/reserve-inventory-quantities.md) í birgðabókhaldi.

Hægt er að komast í birgðabókhald og bókhald framleiðslu í gegnum vinnusvæði **Kostnaðarstjórnunar** og **Kostnaðargreiningar**. Þessi vinnusvæði bjóða upp á ítarlegra yfirlit yfir núverandi stöðu, afkastavísa (KPI) og eftirlit með frávikum. 

Bókhald framleiðslu leyfir notanda að sjá um [Kostnaðaraðferð vinnupöntunar](production-order-cost-analysis.md) í framleiðslu- og runupöntunum ásamt [Bakfærslukostnaðaraðferð](backflush-costing.md) í lean-framleiðslu.

[Kostnaðarstjórnun Power BI-efni](../../dev-itpro/analytics/cost-management-content-pack.md) veitir rekstrarfélagi innsýn í birgðir og birgðir fyrir verk í vinnslu (VÍV) og hvernig kostnaður flæðir í gegnum þær eftir flokki yfir tíma. Upplýsingarnar er einnig hægt að nota sem ítarlega viðbót við fjárhagsskýrslu

### <a name="additional-resources"></a>Frekari upplýsingar

#### <a name="whats-new-and-in-development"></a>Nýjungar og eiginleikar á þróunarstigi

Á [Microsoft Dynamics 365-leiðarvísinum](https://roadmap.dynamics.com/) eru upplýsingar um nýja eiginleika og eiginleika sem eru á þróunarstigi. 

#### <a name="white-paper"></a>Hvítbók
[Útreikningur uppskriftar með notkun kostnaðarskjals](https://mbs.microsoft.com/customersource/northamerica/AX/learning/documentation/white-papers/365operationsbomcalsheet) lýsir því hvernig á að setja upp kostnaðarskjal sem nær yfir efni og framleiðslu og hvernig uppsetningin hefur áhrif á niðurstöður útreiknings á uppskrift. Til að útskýra betur efnisatriðin þá útvegar hann heildstæð dæmi og gögn sem sýna fram á áhrif hinna ýmsu stillinga og skilgreininga. Ekki er ætlast til þess að notandinn fylgi öllum þessum dæmum vegna þess að þetta skjal veitir ekki nægar upplýsingar til að skilgreina þau. Engu að síður getur notandi með grunnþekkingu prófað að spila verkleiðbeiningarnar í þeirri röð sem þær eru útlistaðar hér fyrir neðan. Notið vitneskjuna sem fæst með lestri þessa skjals til að gera greiningu uppskriftaútreiknings. 

-  [Búa til tilbúin afurð](tasks/create-finished-product-2016-02.md)
-  [Búa til hálfunnin vara](tasks/create-semi-finished-product-2016-02.md)
-  [Stofna hráefni](tasks/create-raw-materials-2016-02.md)
-  [Stofna uppskriftir](tasks/create-boms-2016-02.md)
-  [Stofna leiðir](tasks/create-routes-2016-02.md)
-  [Reikna út uppskrift og nota uppbyggingu á einu stigi](tasks/calculate-bom-single-level-structure-2016-02.md)
-  [Reikna út uppskrift og nota uppbyggingu með mörgum stigum](tasks/calculate-bom-multilevel-structure-2016-02.md)


#### <a name="blogs"></a>Blogg
Finna má skoðanir, fréttir og aðrar upplýsingar um kostnaðarstjórnun á [Dynamics AX Manufacturing R&D Team blog](https://blogs.msdn.microsoft.com/axmfg) og [Aðfangakeðjustjórnun í Dynamics AX R&D Team blog](https://blogs.msdn.microsoft.com/dynamicsaxscm). Þó svo sumar þessara færslna hafi verið skrifaðar fyrir eldri útgáfu Kostnaðarstjórnunar eiga sömu hugtök enn við og ferlin eru svipuð í nýjustu útgáfunni.

#### <a name="task-guides"></a>Verkleiðbeiningar
Frekari hjálp er tiltæk sem leiðbeiningar fyrir verkefni. Smellið á hnappinn Hjálp á hvaða síðu sem er til að fá aðgang að verkleiðbeiningum.

