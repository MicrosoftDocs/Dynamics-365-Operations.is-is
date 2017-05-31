---
title: "Mælikvarðar vinnuafls Power BI-efni"
description: "Þetta efnisatriði lýsir Dynamics 365 for Operations - Mælikvarðar vinnuafls Power BI-efnis. Það lýsir einnig hvernig eigi að fara í skýrslur sem eru hafðar með í efnispakkanum, og veitir upplýsingar um gagnalíkan og einingar sem voru notaðar til að búa til efnispakka."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: Operations
ms.custom: 264084
ms.assetid: 8e700583-3a7d-4f5f-9ac8-58c4feed1a02
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 2a3f611d29e041a5f05e3f93fd2330f4218b9dd1
ms.contentlocale: is-is
ms.lasthandoff: 05/25/2017


---

# <a name="workforce-metrics-power-bi-content"></a>Mælikvarðar vinnuafls Power BI-efni

[!include[banner](../includes/banner.md)]


Þetta efnisatriði lýsir Dynamics 365 for Operations - Mælikvarðar vinnuafls Power BI-efnis. Það lýsir einnig hvernig eigi að fara í skýrslur sem eru hafðar með í efnispakkanum, og veitir upplýsingar um gagnalíkan og einingar sem voru notaðar til að búa til efnispakka.

<a name="accessing-the-content-pack"></a>Farið í efnispakkann
--------------------------

Hægt er að finna þjálfunarpakka fyrir mælikvarðar vinnuafls í safninu Samnýttar eignir í Microsoft Dynamics Lifecycle Services (LCS). Upplýsingar um hvernig á að sækja efnispakkann og tengja hann við gögn Microsoft Dynamics 365 for Operations er að finna í [Power BI-efni í LCS frá Microsoft og viðskiptaaðilum þínum](power-bi-content-microsoft-partners.md).

## <a name="reports-that-are-included-in-the-content-pack"></a>Skýrslur sem eru hafðar með í efnispakka
Eftir að þú hefur tengt efnispakkann við gögn Dynamics 365 for Operations, sýnir skýrslan þér fyrirtækjagögn þín. Ef þú hefur aldrei áður notað Microsoft Power BI, má fræðast nánar um það á síðunni [Leiðsögn fyrir Nám fyrir Power BI](https://powerbi.microsoft.com/en-us/guided-learning/?WT.mc_id=PBIService_GetData). Skýrslur sem eru hafðar með í efnispakka hafa bæði gröf og töflur sem innihalda viðbótarupplýsingar. Eftirfarandi tafla lýsir skýrslunum.

| Skýrsla                                           | Innihald                                                                                                                                                                                                            |
|--------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Starfsmannafjöldi eftir fyrirtæki, Deild, Staðsetning | Starfsmannafjöldi eftir fyrirtæki, starfsmannafjöldi eftir deild, starfsmannafjöldi eftir staðsetningu og heildarstarfsmannafjöldi                                                                                                                           |
| Greiningarverk starfsmannafjölda, skref, stjórnun            | Starfsmannafjöldi eftir verki, starfsmannafjöldi eftir skrefi, starfsmannafjöldi eftir stjórnanda og heildarstarfsmannafjöldi                                                                                                                                      |
| Leitnisgreining starfsmannafjölda                         | Starfsmannafjöldi þetta ár samanborið við síðasta ár eftir fyrirtæki og starfsmannavelta síðustu 12 mánaða                                                                                                                        |
| Lýðfræði mannafla                           | Starfsmannafjöldi eftir aldri og kyni, starfsmannafjöldi eftir þjóðerni, starfsmannafjöldi eftir uppgjafahermennskustöðu, starfsmannafjöldi eftir hjúskaparstöðu, fjöldi nemenda í fullu námi, meðaltal lengdar í starfi, meðalaldur og hlutfall kvenna og karla |
| Stöðugreining                                | Opnar stöður eftir deild, stöður til ráðningar, virkar-til-óvirkar stöður og stöður eftir deild                                                                                                   |
| Slitgreining                               | Slit þetta ár samanborið við síðasta ár, slit, meðaltal lengdar einstaklinga í starfi, meðaltal aldur fólks sem fer og ástæða þess að starfsmenn fara                                                                   |
| Fólk eftir deild                             | Starfsmenn með númeri starfsmanns eftir deild, stöðu og upphafs- og lokadagsetningu úthlutunar                                                                                                                       |
| Starfsaldursgreining                               | Meðaltal starfsreynslu eftir fyrirtæki og starfsaldri                                                                                                                                                              |
| Starfsaldur og starfsreynsla í árum               | Starfsmenn eftir fjölda í starfi og starfsafmæli                                                                                                                                                                    |

Hægt er að sía gröf og reiti í þessum skýrslum og festa gröf og reiti á yfirlitið. Nánari upplýsingar um hvernig á að sía og festa í Power BI, sjá [Stofna og Skilgreina Mælaborð](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="understanding-the-data-model-and-entities"></a>Skilja gagnalíkan og einingar
Gögn Dynamics 365 for Operations eru notuð til að mynda skýrslur í mælikvarða vinnuafls. Eftirfarandi tafla sýnir einingar sem efnispakkinn var byggður á.

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
| Vinnuafl\_JobPerferredSkill      |                                                                                                            |                                                                                                                                                                                                                                                                                                                                  |
| Vinnuafl\_PastPositionAssignment | Upphafsdagur, lokadagur, breytingardagur og vinnsla                                                           | Vinnuafl\_CalendarOffset Workforce\_Date Workforce\_Job Workforce\_Staða                                                                                                                                                                                                                                                     |
| Vinnuafl\_Performance            | Mat, lýsing og matslíkan                                                                      | Vinnuafl\_CurrentWorker Vinnuafl\_TerminatedWorker Vinnuafl\_WorkerTrend                                                                                                                                                                                                                                                       |
| Vinnuafl\_PersonSkill            | Færni og stig                                                                                            | Vinnuafl\_Skill                                                                                                                                                                                                                                                                                                                 |
| Vinnuafl\_PersonSkillAnalysis    | Vottun, færni og stig                                                                                | Vinnuafl\_Skill Vinnuafl\_WorkerName                                                                                                                                                                                                                                                                                           |
| Vinnuafl\_Position               | Deild, FTE, staða, gerð stöðu og Titill                                                        | Vinnuafl\_CurrentPosition Vinnuafl\_CurrentWorker                                                                                                                                                                                                                                                                              |
| Vinnuafl\_PositionTrend          | Staða yfir tími, FTE, og vinnsla                                                                          | Vinnuafl\_CalendarOffset Workforce\_Date Workforce\_Job Workforce\_Staða                                                                                                                                                                                                                                                     |
| Vinnuafl\_ReportsToWorkerName    | Fornafn, eftirnafn, og fullt nafn                                                                       | Vinnuafl\_CurrentWorker Vinnuafl\_TerminatedWorker Vinnuafl\_WorkerTrend                                                                                                                                                                                                                                                       |
| Vinnuafl\_Skill                  | Hæfni, gerð hæfni og mat                                                                              | Vinnuafl\_PersonSkill Workforce\_PersonSkillAnalysis                                                                                                                                                                                                                                                                            |
| Vinnuafl\_TerminatedWorker       | Starfsfólk sem er hætt, starfslokadagsetning, Titill, staða, og starf                                             | Vinnuafl\_Vinnuafl fyrirtækis\_Vinnuafl bóta\_GeographicLocation Workforce\_Performance Workforce\_WorkerName Workforce\_ReportsToWorkerName Workforce\_CalendarOffset Workforces\_Date Workforce\_WorkerTitle Workforce\_Demographics Workforce\_Employment Workforce\_Job Workforce\_Position Workforce\_WorkerBenefit |
| Vinnuafl\_WorkerBenefit          | Gildisdagsetning, fríðindavalkostur, fríðindaáætlun, og fríðindi gerð                                             | Vinnuafl\_CurrentWorker Vinnuafl\_TerminatedWorker Vinnuafl\_WorkerTrend                                                                                                                                                                                                                                                       |
| Vinnuafl\_WorkerName             | Fornafn, eftirnafn, og fullt nafn                                                                       | Vinnuafl\_CurrentWorker Workforce\_TerminatedWorker Workorce\_WorkerTrend Workforce\_PersonSkillAnalysis                                                                                                                                                                                                                        |
| Vinnuafl\_WorkerTitle            | Titill og starfsaldursdagsetning                                                                                   | Vinnuafl\_CurrentWorker Vinnuafl\_TerminatedWorker Vinnuafl\_WorkerTrend                                                                                                                                                                                                                                                       |
| Vinnuafl\_WorkerTrend             | Starfsfólk yfir tíma, starfsmannafjöldi, fyrirtæki og staða                                                        | Vinnuafl\_Vinnuafl fyrirtækis\_Vinnuafl bóta\_GeographicLocation Workforce\_Performance Workforce\_WorkerName Workforce\_ReportsToWorkerName Workforce\_CalendarOffset Workforces\_Date Workforce\_WorkerTitle Workforce\_Demographics Workforce\_Employment Workforce\_Job Workforce\_WorkerBenefit                     |

Þessar einingar voru notaðar til að stofna reiknaðar mælieiningar í gagnalíkaninu. Þessar reikuðu mælieiningar eru síðan notaðar til að stofna reiknaðar ráðstafanir til að reikna út afkastavísar (KPI ) og skýrslur sem eru notaðar í efnispakkanum. Eigi taka á með viðbótarútreikning í skýrslum og mælaborði er hægt að sækja og breyta CompensationandBenefits.pbix-skrá í LCS. Þessi skrá er sjálfgefið gagnalíkan sem var notað til að stofna efnispakkann. Eftir að breytingarnar hafa verið gerðar er hægt að stofna efnispakka fyrirtækis og mælaborð sem innihalda upplýsingar sem hefur verið bætt við.

## <a name="additional-resources"></a>Frekari upplýsingar
Hér eru gagnlegir tenglar sem tengjast einingar og að búa til Power BI-efni:

-   [Gagnaeiningar](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/)
-   [Stofnun efnispakka fyrirtækis ](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   [Gera gagnalíkön með því að nota Power BI](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [Bæta Power BI-reitum við vinnusvæði](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/07/06/pinning-power-bi-reports-to-dynamics-ax-client/)





