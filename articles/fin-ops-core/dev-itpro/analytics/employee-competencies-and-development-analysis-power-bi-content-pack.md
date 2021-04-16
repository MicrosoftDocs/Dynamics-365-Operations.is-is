---
title: Hæfni og þróun starfsmanna Power BI efni
description: Þetta efnisatriði lýsir starfsmannahæfni og -þróun Power BI efni.
author: jcart1106
ms.date: 12/19/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 263894
ms.assetid: 7d375d8a-b2de-4bec-b575-93d1d4521b79
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 43a6d825de5d8e012d9ccbfccc5d8c708f248981
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5751287"
---
# <a name="employee-competencies-and-development-power-bi-content"></a>Hæfni og þróun starfsmanna Power BI efni

[!include [banner](../includes/banner.md)]

Þetta efnisatriði lýsir starfsmannahæfni og -þróun Power BI efni. 

## <a name="reports-that-are-included-in-the-content-pack"></a>Skýrslur sem eru hafðar með í efnispakka
Eftir að þú hefur tengt efnispakkann við gögnin sýna skýrslurnar fyrirtækjagögnin þín. Ef þú hefur aldrei áður notað Microsoft Power BI, má fræðast nánar um það á síðunni [Leiðsögn fyrir Nám fyrir Power BI](https://powerbi.microsoft.com/guided-learning/?WT.mc_id=PBIService_GetData). Skýrslur sem eru hafðar með í efnispakka hafa bæði gröf og töflur sem innihalda viðbótarupplýsingar. Eftirfarandi tafla lýsir skýrslunum.

| Skýrsla                            | Innihald                                               |
|-----------------------------------|--------------------------------------------------------|
| Greining á hæfni og þróun | Hæfnisgerðir teymismeðlima og hæfni teymismeðlima eftir gerð |
| Hæfniyfirlit                     | Hæfniyfirlit fyrir valinn starfsmann                |
| Hæfnigreining                    | Hæfni eftir gerð og einkunn                              |

Hægt er að sía gröf og reiti í þessum skýrslum og festa gröf og reiti á yfirlitið. Nánari upplýsingar um hvernig á að sía og festa í Power BI, sjá [Stofna og Skilgreina Mælaborð](https://powerbi.microsoft.com/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="understanding-the-data-model-and-entities"></a>Skilja gagnalíkan og einingar
Forritsgögn eru notuð til að fylla út skýrslurnar í efnispakka starfsmannahæfni og -þróunar. Eftirfarandi tafla sýnir einingar sem efnispakkinn var byggður á.

| Eining                            | Innihald                                                                                                   | Vensl við aðra lögaðila |
|-----------------------------------|------------------------------------------------------------------------------------------------------------|-----------------------------------|
| Vinnuafl\_CalendarOffset         | Mótbókanir dagatals til að sneiða skýrslur                                                                          | |
| Vinnuafl\_Company                | Fyrirtæki til að sía skýrsla eftir                                                                             | |
| Vinnuafl\_Compensation           | Launataxti og tíðni yfir tíma                                                                           | |
| Vinnuafl\_CurrentCompensation    | Launataxti og tíðni frá og með núverandi dagsetningu                                                              | Vinnuafl\_Fyrirtæki, vinnuafl\_CurrentCompensation, Workforce\_Demographics, Workforce\_Job, Workforce\_Position |
| Vinnuafl\_CurrentPosition        | Stöður frá og með núgildandi dagsetningu, ígildi fulls starfs (FTE), opin staða og virkar-til-óvirkar stöður | Vinnuafl\_Job Workforce\_Position |
| Vinnuafl\_CurrentWorker          | Starfsmenn frá og með núverandi dagsetningu, aldri og starfsmannafjölda                                                         | Vinnuafl\_Company Workforce\_Compensation, Workforce\_GeographicLocation, Workforce\_Performance, Workforce\_PersonSkill, Workforce\_WorkerName, Workforce\_ReportsToWorkerName, Workforce\_WorkerTitle, Workforce\_Demographics, Workforce\_Job, Workforce\_Employment, Workforce\_Position |
| Vinnuafl\_Dagsetning                   | Dagar, vikur, mánuðir og ár                                                                             | |
| Vinnuafl\_Lýðfræði           | Fæðingardagur, kyn, þjóðernisuppruni og hjúskapaarstaða                                                   | |
| Vinnuafl\_Ráðning             | Upphafsdagur, lokadagur og breytingardagur                                                                  | |
| Vinnuafl\_GeographicLocation     | Borg, sýsla, póstnúmer og fylki eða Sveitarfélag                                                           | |
| Vinnuafl\_Starf                    | Aðgerð, gerð og Titill                                                                                  | |
| Vinnuafl\_JobPerferredSkill      | Mikilvægi, einkunn, hæfni og hæfnisstig                                                                 | Vinnuafl\_Skill, Workforce\_Job |
| Vinnuafl\_PastPositionAssignment | Upphafsdagur, lokadagur, breytingardagur og vinnsla                                                           | Vinnuafl\_CalendarOffset, Workforce\_Date, Workforce\_Job, Workforce\_Staða |
| Vinnuafl\_Performance            | Mat, lýsing og matslíkan                                                                      | |
| Vinnuafl\_PersonSkill            | Stig, dagsetning stigs og hæfni                                                                               | Vinnuafl\_Skill |
| Vinnuafl\_PersonSkillAnalysis    | Vottun, stig, dagsetning stigs og hæfni                                                                    | Vinnuafl\_WorkerName, Workforce\_Skill |
| Vinnuafl\_Position               | Deild, FTE, staða, gerð stöðu og Titill                                                        | |
| Vinnuafl\_PositionTrend          | Staða yfir tími, FTE, og vinnsla                                                                          | Vinnuafl\_CalendarOffset, Workforce\_Date, Workforce\_Job, Workforce\_Staða |
| Vinnuafl\_ReportsToWorkerName    | Fornafn, eftirnafn, og fullt nafn                                                                       | |
| Vinnuafl\_Skill                  | Hæfni, gerð hæfni og mat                                                                              | |
| Vinnuafl\_TerminatedWorker       | Starfsfólk sem er hætt, starfslokadagsetning, Titill, staða, og starf                                             | Vinnuafl\_Company, Workforce\_Compensation, Workforce\_GeographicLocation, Workforce\_Performance, Workforce\_WorkerName, Workforce\_ReportsToWorkerName, Workforce\_CalendarOffset, Workforces\_Date, Workforce\_WorkerTitle, Workforce\_Demographics, Workforce\_Employment, Workforce\_Job, Workforce\_Position |
| Vinnuafl\_WorkerName             | Fornafn, eftirnafn, og fullt nafn                                                                       | |
| Vinnuafl\_WorkerTitle            | Titill og starfsaldursdagsetning                                                                                   | |
| Vinnuafl\_WorkerTrend             | Starfsfólk yfir tíma, starfsmannafjöldi, fyrirtæki og staða                                                        | Vinnuafl\_Company, Workforce\_Compensation, Workforce\_GeographicLocation, Workforce\_Performance, Workforce\_WorkerName, Workforce\_ReportsToWorkerName, Workforce\_CalendarOffset, Workforces\_Date, Workforce\_WorkerTitle, Workforce\_Demographics, Workforce\_Employment, Workforce\_Job |


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]