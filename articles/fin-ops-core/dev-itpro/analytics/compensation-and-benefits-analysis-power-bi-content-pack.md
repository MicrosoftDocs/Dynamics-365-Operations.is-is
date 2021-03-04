---
title: Launa- og fríðindaskýrslur Power BI efni
description: Þetta efnisatriði lýsir Power BI-efninu Laun og fríðindi.
author: jcart1106
manager: AnnBe
ms.date: 12/19/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 263914
ms.assetid: 18634bb5-3341-42f2-9cc9-7b04708b506b
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 69149f55371f64b4907f6040e9de03843fc11717
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/05/2020
ms.locfileid: "4687207"
---
# <a name="compensation-and-benefits-power-bi-content"></a>Launa- og fríðindaskýrslur Power BI efni

[!include [banner](../includes/banner.md)]

Þetta efnisatriði lýsir Power BI-efninu Laun og fríðindi. 

## <a name="reports-that-are-included-in-the-content-pack"></a>Skýrslur sem eru hafðar með í efnispakka
Eftir að þú hefur tengt efnispakkann við gögnin sýna skýrslurnar fyrirtækjagögnin þín. Ef þú hefur aldrei áður notað Microsoft Power BI, má fræðast nánar um það á síðunni [Leiðsögn fyrir Nám fyrir Power BI](https://powerbi.microsoft.com/guided-learning/?WT.mc_id=PBIService_GetData). Skýrslur sem eru hafðar með í efnispakka hafa bæði gröf og töflur sem innihalda viðbótarupplýsingar. Eftirfarandi tafla lýsir skýrslunum.

| Skýrsla                     | Innihald                                                                                                                              |
|----------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| COMP og Fríðindi Greining | Starfsmenn á tímakaupi og starfsmenn á launum eftir fyrirtæki, meðaltal tímakaups, meðaltal launa, starfsmenn eftir ráðningargerð og áætlun skráningar |
| Fríðindi starfsmanna          | Starfsmannaskráning eftir völdum fríðindum                                                                                               |

Hægt er að sía gröf og reiti í þessum skýrslum og festa gröf og reiti á yfirlitið. Nánari upplýsingar um hvernig á að sía og festa í Power BI, sjá [Stofna og Skilgreina Mælaborð](https://powerbi.microsoft.com/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="understanding-the-data-model-and-entities"></a>Skilja gagnalíkan og einingar
Forritsgögnin eru notuð til að mynda skýrslur í efnispakkanum Laun og fríðindi. Eftirfarandi tafla sýnir einingar sem efnispakkinn var byggður á.

| Eining                            | Innihald                                                                                                   | Vensl við aðra lögaðila |
|-----------------------------------|------------------------------------------------------------------------------------------------------------|-----------------------------------|
| Vinnuafl\_CalendarOffset         | Mótbókanir dagatals til að sneiða skýrslur                                                                          | Vinnuafl\_PastPositionAssignment, Workforce\_PositionTrend, Workforce\_WorkerTrend, Workforce\_TerminatedWorker |
| Vinnuafl\_Company                | Fyrirtæki til að sía skýrsla eftir                                                                             | Vinnuafl\_CurrentCompensation, Workforce\_CurrentWorker, Workforce\_TerminatedWorker, Workforce\_WorkerTrend |
| Vinnuafl\_Compensation           | Launataxti og tíðni yfir tíma                                                                           | Vinnuafl\_CurrentCompensation, Workforce\_CurrentWorker, Workforce\_TerminatedWorker, Workforce\_WorkerTrend |
| Vinnuafl\_CurrentCompensation    | Launataxti og tíðni frá og með núverandi dagsetningu                                                              | Vinnuafl\_Fyrirtæki, Vinnuafl\_Compensation, Workforce\_Demographics, Workforce\_Job, Workforce\_Position |
| Vinnuafl\_CurrentPosition        | Stöður frá og með núgildandi dagsetningu, ígildi fulls starfs (FTE), opin staða og virkar-til-óvirkar stöður | Vinnuafl\_Job, Workforce\_Position |
| Vinnuafl\_CurrentWorker          | Starfsmenn frá og með núverandi dagsetningu, aldri og starfsmannafjölda                                                         | Vinnuafl\_Company, Workforce\_Compensation, Workforce\_GeographicLocation, Workforce\_Performance, Workforce\_WorkerName, Workforce\_ReportsToWorkerName, Workforce\_WorkerTitle, Workforce\_Demographics, Workforce\_Job, Workforce\_Employment, Workforce\_Position, Workforce\_WorkerBenefit |
| Vinnuafl\_Dagsetning                   | Dagar, vikur, mánuðir og ár                                                                             | Vinnuafl\_PastPositionAssignment, Workforce\_PositionTrend, Workforce\_TerminatedWorker, Workforce\_WorkerTrend |
| Vinnuafl\_Lýðfræði           | Fæðingardagur, kyn, þjóðernisuppruni og hjúskapaarstaða                                                   | Vinnuafl\_CurrentWorker, Workforce\_TerminatedWorker, Workforce\_WorkerTrend |
| Vinnuafl\_Ráðning             | Upphafsdagur, lokadagur og breytingardagur                                                                  | Vinnuafl\_CurrentWorker, Workforce\_TerminatedWorker, Workforce\_WorkerTrend |
| Vinnuafl\_GeographicLocation     | Borg, sýsla, póstnúmer og fylki eða Sveitarfélag                                                           | Vinnuafl\_CurrentWorker, Workforce\_TerminatedWorker, Workforce\_WorkerTrend |
| Vinnuafl\_Starf                    | Aðgerð, gerð og Titill                                                                                  | Vinnuafl\_CurrentPosition, Workforce\_CurrentWorker |
| Vinnuafl\_PastPositionAssignment | Upphafsdagur, lokadagur, breytingardagur og vinnsla                                                           | Vinnuafl\_CalendarOffset, Workforce\_Date, Workforce\_Job, Workforce\_Staða |
| Vinnuafl\_Performance            | Mat, lýsing og matslíkan                                                                      | Vinnuafl\_CurrentWorker, Workforce\_TerminatedWorker, Workforce\_WorkerTrend |
| Vinnuafl\_Position               | Deild, FTE, staða, gerð stöðu og Titill                                                        | Vinnuafl\_CurrentPosition, Workforce\_CurrentWorker |
| Vinnuafl\_PositionTrend          | Staða yfir tími, FTE, og vinnsla                                                                          | Vinnuafl\_CalendarOffset, Workforce\_Date, Workforce\_Job, Workforce\_Staða |
| Vinnuafl\_ReportsToWorkerName    | Fornafn, eftirnafn, og fullt nafn                                                                       | Vinnuafl\_CurrentWorker, Workforce\_TerminatedWorker, Workforce\_WorkerTrend |
| Vinnuafl\_Skill                  | Hæfni, gerð hæfni og mat                                                                              | |
| Vinnuafl\_TerminatedWorker       | Starfsfólk sem er hætt, starfslokadagsetning, Titill, staða, og starf                                             | Vinnuafl\_Fyrirtæki, vinnuafl\_Vinnuafl, laun\_GeographicLocation, Workforce\_Performance, Workforce\_WorkerName, Workforce\_ReportsToWorkerName, Workforce\_CalendarOffset, Workforces\_Date, Workforce\_WorkerTitle, Workforce\_Demographics, Workforce\_Employment, Workforce\_Job, Workforce\_Position, Workforce\_WorkerBenefit |
| Vinnuafl\_WorkerBenefit          | Gildisdagsetning, fríðindavalkostur, fríðindaáætlun, og fríðindi gerð                                             | Vinnuafl\_CurrentWorker, Workforce\_TerminatedWorker, Workforce\_WorkerTrend |
| Vinnuafl\_WorkerName             | Fornafn, eftirnafn, og fullt nafn                                                                       | Vinnuafl\_CurrentWorker, Workforce\_TerminatedWorker, Workforce\_WorkerTrend |
| Vinnuafl\_WorkerTitle            | Titill og starfsaldursdagsetning                                                                                   | Vinnuafl\_CurrentWorker, Workforce\_TerminatedWorker, Workforce\_WorkerTrend |
| Vinnuafl\_WorkerTrend            | Starfsfólk yfir tíma, starfsmannafjöldi, fyrirtæki og staða                                                        | Vinnuafl\_Fyrirtæki, vinnuafl\_Laun, vinnuafl\_GeographicLocation, Workforce\_Performance, Workforce\_WorkerName, Workforce\_ReportsToWorkerName, Workforce\_CalendarOffset, Workforces\_Date, Workforce\_WorkerTitle, Workforce\_Demographics, Workforce\_Employment, Workforce\_Job, Workforce\_WorkerBenefit |


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]