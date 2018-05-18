---
title: "Laun og fríðindi Power BI efni"
description: "Þetta efnisatriði lýsir Finance and Operations - Compensation and Benefits Power BI."
author: jcart1106
manager: AnnBe
ms.date: 12/19/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.custom: 263914
ms.assetid: 18634bb5-3341-42f2-9cc9-7b04708b506b
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: cb43245afe578341251b140383a3b03ba2abd962
ms.openlocfilehash: 510064a462258b2a632eaa2a5ffd341950775b89
ms.contentlocale: is-is
ms.lasthandoff: 12/19/2017

---

# <a name="compensation-and-benefits-power-bi-content"></a>Laun og fríðindi Power BI efni

[!include [banner](../includes/banner.md)]

Þetta efnisatriði lýsir Finance and Operations - Compensation and Benefits Power BI. 

## <a name="reports-that-are-included-in-the-content-pack"></a>Skýrslur sem eru hafðar með í efnispakka
Eftir að þú hefur tengt efnispakkann við gögn Finance and Operations, sýnir skýrslan þér fyrirtækjagögn þín. Ef þú hefur aldrei áður notað Microsoft Power BI, má fræðast nánar um það á síðunni [Leiðsögn fyrir Nám fyrir Power BI](https://powerbi.microsoft.com/en-us/guided-learning/?WT.mc_id=PBIService_GetData). Skýrslur sem eru hafðar með í efnispakka hafa bæði gröf og töflur sem innihalda viðbótarupplýsingar. Eftirfarandi tafla lýsir skýrslunum.

| Skýrsla                     | Innihald                                                                                                                              |
|----------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| COMP og Fríðindi Greining | Starfsmenn á tímakaupi og starfsmenn á launum eftir fyrirtæki, meðaltal tímakaups, meðaltal launa, starfsmenn eftir ráðningargerð og áætlun skráningar |
| Fríðindi starfsmanna          | Starfsmannaskráning eftir völdum fríðindum                                                                                               |

Hægt er að sía gröf og reiti í þessum skýrslum og festa gröf og reiti á yfirlitið. Nánari upplýsingar um hvernig á að sía og festa í Power BI, sjá [Stofna og Skilgreina Mælaborð](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="understanding-the-data-model-and-entities"></a>Skilja gagnalíkan og einingar
Finance and Operations er notað til að mynda skýrslur í efnispakka Compensation and Benefits. Eftirfarandi tafla sýnir einingar sem efnispakkinn var byggður á.

| Eining                            | Innihald                                                                                                   | Vensl við aðra lögaðila                                                                                                                                                                                                                                                                                                |
|-----------------------------------|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Vinnuafl\_CalendarOffset         | Mótbókanir dagatals til að sneiða skýrslur                                                                          | Vinnuafl\_PastPositionAssignment Workforce\_PositionTrend Workorce\_WorkerTrend Workforce\_TerminatedWorker                                                                                                                                                                                                                     |
| Vinnuafl\_Company                | Fyrirtæki til að sía skýrsla eftir                                                                             | Vinnuafl\_CurrentCompensation Workforce\_CurrentWorker Workforce\_TerminatedWorker Workorce\_WorkerTrend                                                                                                                                                                                                                        |
| Vinnuafl\_Compensation           | Launataxti og tíðni yfir tíma                                                                           | Vinnuafl\_CurrentCompensation Workforce\_CurrentWorker Workforce\_TerminatedWorker Workorce\_WorkerTrend                                                                                                                                                                                                                        |
| Vinnuafl\_CurrentCompensation    | Launataxti og tíðni frá og með núverandi dagsetningu                                                              | Vinnuafl\_Vinnuafl fyrirtækis\_Compensation Workforce\_Demographics Workforce\_Job Workforce\_Position                                                                                                                                                                                                                            |
| Vinnuafl\_CurrentPosition        | Stöður frá og með núgildandi dagsetningu, ígildi fulls starfs (FTE), opin staða og virkar-til-óvirkar stöður | Vinnuafl\_Job Workforce\_Position                                                                                                                                                                                                                                                                                               |
| Vinnuafl\_CurrentWorker          | Starfsmenn frá og með núverandi dagsetningu, aldri og starfsmannafjölda                                                         | Vinnuafl\_Company Workforce\_Compensation Workforce\_GeographicLocation Workforce\_Performance Workforce\_WorkerName Workforce\_ReportsToWorkerName Workforce\_WorkerTitle Workforce\_Demographics Workforce\_Job Workforce\_Employment Workforce\_Position Workforce\_WorkerBenefit                                            |
| Vinnuafl\_Dagsetning                   | Dagar, vikur, mánuðir og ár                                                                             | Vinnuafl\_PastPositionAssignment Workforce\_PositionTrend Workforce\_TerminatedWorker Workorce\_WorkerTrend                                                                                                                                                                                                                     |
| Vinnuafl\_Lýðfræði           | Fæðingardagur, kyn, þjóðernisuppruni og hjúskapaarstaða                                                   | Vinnuafl\_CurrentWorker Vinnuafl\_TerminatedWorker Vinnuafl\_WorkerTrend                                                                                                                                                                                                                                                       |
| Vinnuafl\_Ráðning             | Upphafsdagur, lokadagur og breytingardagur                                                                  | Vinnuafl\_CurrentWorker Vinnuafl\_TerminatedWorker Vinnuafl\_WorkerTrend                                                                                                                                                                                                                                                       |
| Vinnuafl\_GeographicLocation     | Borg, sýsla, póstnúmer og fylki eða Sveitarfélag                                                           | Vinnuafl\_CurrentWorker Vinnuafl\_TerminatedWorker Vinnuafl\_WorkerTrend                                                                                                                                                                                                                                                       |
| Vinnuafl\_Starf                    | Aðgerð, gerð og Titill                                                                                  | Vinnuafl\_CurrentPosition Vinnuafl\_CurrentWorker                                                                                                                                                                                                                                                                              |
| Vinnuafl\_PastPositionAssignment | Upphafsdagur, lokadagur, breytingardagur og vinnsla                                                           | Vinnuafl\_CalendarOffset Workforce\_Date Workforce\_Job Workforce\_Staða                                                                                                                                                                                                                                                     |
| Vinnuafl\_Performance            | Mat, lýsing og matslíkan                                                                      | Vinnuafl\_CurrentWorker Vinnuafl\_TerminatedWorker Vinnuafl\_WorkerTrend                                                                                                                                                                                                                                                       |
| Vinnuafl\_Position               | Deild, FTE, staða, gerð stöðu og Titill                                                        | Vinnuafl\_CurrentPosition Vinnuafl\_CurrentWorker                                                                                                                                                                                                                                                                              |
| Vinnuafl\_PositionTrend          | Staða yfir tími, FTE, og vinnsla                                                                          | Vinnuafl\_CalendarOffset Workforce\_Date Workforce\_Job Workforce\_Staða                                                                                                                                                                                                                                                     |
| Vinnuafl\_ReportsToWorkerName    | Fornafn, eftirnafn, og fullt nafn                                                                       | Vinnuafl\_CurrentWorker Vinnuafl\_TerminatedWorker Vinnuafl\_WorkerTrend                                                                                                                                                                                                                                                       |
| Vinnuafl\_Skill                  | Hæfni, gerð hæfni og mat                                                                              |                                                                                                                                                                                                                                                                                                                                  |
| Vinnuafl\_TerminatedWorker       | Starfsfólk sem er hætt, starfslokadagsetning, Titill, staða, og starf                                             | Vinnuafl\_Vinnuafl fyrirtækis\_Vinnuafl bóta\_GeographicLocation Workforce\_Performance Workforce\_WorkerName Workforce\_ReportsToWorkerName Workforce\_CalendarOffset Workforces\_Date Workforce\_WorkerTitle Workforce\_Demographics Workforce\_Employment Workforce\_Job Workforce\_Position Workforce\_WorkerBenefit |
| Vinnuafl\_WorkerBenefit          | Gildisdagsetning, fríðindavalkostur, fríðindaáætlun, og fríðindi gerð                                             | Vinnuafl\_CurrentWorker Vinnuafl\_TerminatedWorker Vinnuafl\_WorkerTrend                                                                                                                                                                                                                                                       |
| Vinnuafl\_WorkerName             | Fornafn, eftirnafn, og fullt nafn                                                                       | Vinnuafl\_CurrentWorker Vinnuafl\_TerminatedWorker Vinnuafl\_WorkerTrend                                                                                                                                                                                                                                                       |
| Vinnuafl\_WorkerTitle            | Titill og starfsaldursdagsetning                                                                                   | Vinnuafl\_CurrentWorker Vinnuafl\_TerminatedWorker Vinnuafl\_WorkerTrend                                                                                                                                                                                                                                                       |
| Vinnuafl\_WorkerTrend             | Starfsfólk yfir tíma, starfsmannafjöldi, fyrirtæki og staða                                                        | Vinnuafl\_Vinnuafl fyrirtækis\_Vinnuafl bóta\_GeographicLocation Workforce\_Performance Workforce\_WorkerName Workforce\_ReportsToWorkerName Workforce\_CalendarOffset Workforces\_Date Workforce\_WorkerTitle Workforce\_Demographics Workforce\_Employment Workforce\_Job Workforce\_WorkerBenefit                     |







