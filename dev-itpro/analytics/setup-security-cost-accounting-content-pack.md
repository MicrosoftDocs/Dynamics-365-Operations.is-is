---
title: "Setja upp öryggisbúnað fyrir greiningu kostnaðarbókhald Power BI efni"
description: "Í þessu efnisatriði er útskýrt hvernig hægt propagate aðgang á færslustigi í kostnaðarbókhaldi í línu á færslustigi í Microsoft Power BI. Þessi virkni hjálpar til við að tryggja samræmda notendur sjá aðeins Power viðskiptagreindargögn sem þeir fá aðgang að."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: Operations
ms.custom: 270294
ms.assetid: 3a7ba8b0-ac57-4159-9cd8-4308f6021f36
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 388b6398488e6f316c1ec07a00182e81c1dc8d08
ms.openlocfilehash: 1e42622e7621c645d7eda3299f78c34c7e41a251
ms.lasthandoff: 03/31/2017


---

# <a name="set-up-security-for-the-cost-accounting-analysis-power-bi-content"></a>Setja upp öryggisbúnað fyrir greiningu kostnaðarbókhald Power BI efni

Í þessu efnisatriði er útskýrt hvernig hægt propagate aðgang á færslustigi í kostnaðarbókhaldi í línu á færslustigi í Microsoft Power BI. Þessi virkni hjálpar til við að tryggja samræmda notendur sjá aðeins Power viðskiptagreindargögn sem þeir fá aðgang að.

<a name="overview"></a>Yfirlit
--------

Í **kostnaðarbókhald analysis** efni Microsoft Power BI notar öryggi á línustigi Power BI til að takmarka aðgang notenda. Öryggi á grundvelli-aðgangsstig stigveldisskipan sem sett er upp í færibreytum kostnaðarbókhalds. Nánari upplýsingar um í **kostnaðarbókhald analysis** Power BI innihald, sjá [kostnaðarbókhald analysis Power BI efni](cost-accounting-analysis-content-pack.md).

## <a name="setup"></a>Uppsetning
Eigandi innihald Power BI að propagate aðgang á færslustigi á Power BI, verður að fylgja eftirfarandi skrefum. **Athugasemd:** notandann sem gefur út í **kostnaðarbókhald analysis** Power BI efni verður sjálfkrafa eiganda. Setja má upp öryggi í Power BI aðeins inn eiganda. Þar að auki er fyrr en inn eiganda bætir annarra notenda á PowerBI.com enginn við eitt nema eigandi er hægt að sjá hvaða gögn í **kostnaðarbókhald analysis** Power BI efni.

1.  Birta Power BI í skilgreiningarskránni.
2.  Innskráning á PowerBI.com.
3.  Finna dataset fyrir í **kostnaðarbókhald analysis** Power BI efni.
4.  Opna síðuna öryggi. 

    [![Opna síðuna öryggi](https://msdynamics.blob.core.windows.net/media/2017/02/CA-picture-1.png)](https://msdynamics.blob.core.windows.net/media/2017/02/CA-picture-1.png)

5.  Í **Kostnaður hlut fjármálastjóra** hlutverk er þegar stofnað. Bæta við öðrum aðilum sem eru hluti af stigveldisskipan aðgangsstig kostnaðarbókhalds. 

    [![Bæta við meðlimum](https://msdynamics.blob.core.windows.net/media/2017/02/CA-picture-2.png)](https://msdynamics.blob.core.windows.net/media/2017/02/CA-picture-2.png)

Notendur sem er bætt við í **Kostnaður hlut fjármálastjóra** hlutverk sjá aðeins gögnin sem þeir hafa heimild til að sjá, samkvæmt skilgreiningu í stigveldisskipan aðgangsstig kostnaðarbókhalds. **Athugasemd:** Línu á færslustigi við reitir og skýrslur í Microsoft Dynamics 365 fyrir Aðgerðir sem eru innfelld úr Power BI.

## <a name="updating-security"></a>Uppfærir öryggi
Ef uppfærslur eru gerðar á aðgang á færslustigi í kostnaðarbókhaldi, og Power BI til að endurspegla þær uppfærslur á, þarf að uppfæra einingar verslun fyrir á **kostnaðarbókhald analysis** Power BI efni. Eftir uppfærslu verslun einingar úr Dynamics 365 aðgerða er lokið verður að uppfæra gervingar á PowerBI.com. Nánari upplýsingar um hvernig á að gera uppfærslu verslun einingar í [Uppfærsla einingar verslun](power-bi-integration-entity-store.md#update-entity-store). Eigandi er **kostnaðarbókhald analysis** Power BI efni einnig gert uppfærslu einingar verslun ef nýja notendur fá aðgang að stigveldisskipan. Þar að auki er eigandi verður að bæta við nýju notendum að á **Kostnaður hlut fjármálastjóra** hlutverk í PowerBI.com, svo sem öryggi á línustigi er notað fyrir þær.

## <a name="disabling-security"></a>Gera öryggi
Gerum við fyrir fyrirtækið vill að takmarka aðgang gögn. Ef af einhverri ástæðu, eru öryggi færibreyturnar óvirkan þegar kostnaðarbókhald er keyrt, eigandinn verður að bæta notendum við í **kostnaðarbókari** hlutverk í Power BI í staðinn. Ef öryggislykillinn er breytt úr virk staða í óvirkri stöðu, er góð hugmynd að fjarlægja notendur úr á **Kostnaður hlut fjármálastjóra** hlutverk. Og öfugt ef virkja öryggisstillingar aftur. Notendur geta tilheyrt bæði hlutverk. Sameiginlegar aðgang er sameiningu bæði hlutverkum. Í því case yfir í **kostnaðarbókhald analysis** Power BI innihald notendur sem aðgang sameiginlegar hafa unrestricted gagnaaðgangur. Ef skal markmiði er að nota takmarkaða aðgang notenda verður að úthluta eingöngu til í **Kostnaður hlut fjármálastjóra** hlutverk. Öryggi á línustigi uppfærslurnar taki strax. Notendur verða fyrir áhrifum ætti að endurnýja vöfrum þeirra.

## <a name="additional-resources"></a>Frekari upplýsingar
Sjá frekari upplýsingar um öryggi á línustigi Power BI, [umsjón Með öryggi á líkanið í Power BI](https://powerbi.microsoft.com/en-us/documentation/powerbi-admin-rls/#manage-security-on-your-model).


