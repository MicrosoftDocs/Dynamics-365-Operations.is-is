---
title: "Hæfni starfsmanna og Þróun Power BI innihald"
description: "Þetta efnisatriði lýsir Dynamics 365 aðgerða - Hæfni Starfsmanna og Þróun Power BI efni. Það útskýrt hvernig á að fá aðgang að skýrslunum sem eru innifaldar í innihald þjónustupakka og upplýsingar um gagnalíkan og einingar sem voru notaðir til að búa til innihald þjónustupakka."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: Operations
ms.custom: 263894
ms.assetid: 7d375d8a-b2de-4bec-b575-93d1d4521b79
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 388b6398488e6f316c1ec07a00182e81c1dc8d08
ms.openlocfilehash: 1fd6f978b6a871f9f7d3d5e91ab3e0aac789ae88
ms.lasthandoff: 03/31/2017


---

# <a name="employee-competencies-and-development-power-bi-content"></a>Hæfni starfsmanna og Þróun Power BI innihald

Þetta efnisatriði lýsir Dynamics 365 aðgerða - Hæfni Starfsmanna og Þróun Power BI efni. Það útskýrt hvernig á að fá aðgang að skýrslunum sem eru innifaldar í innihald þjónustupakka og upplýsingar um gagnalíkan og einingar sem voru notaðir til að búa til innihald þjónustupakka.

<a name="accessing-the-content-pack"></a>Fara í hugbúnaðarhlutartréð innihaldi pakka
--------------------------

Hægt er að finna Hæfni Starfsmanna og Þróun innihaldi pakka í Samnýttum eignir safn í Microsoft Dynamics Lifecycle Services (LCS). Nánari upplýsingar um hvernig á að sækja innihald þjónustupakka og tengja hana við Microsoft Dynamics 365 fyrir Aðgerðir í [Power BI efni í LCS frá Microsoft og for your viðskiptaaðila](power-bi-content-microsoft-partners.md).

## <a name="reports-that-are-included-in-the-content-pack"></a>Skýrslur sem eru hafðar með í innihald þjónustupakka
Eftir að þú hefur verið tengdur innihald þjónustupakka skal Dynamics 365 fyrir Aðgerðir, skýrslur sem sýna gögn fyrirtækisins. Ef aldrei hefur verið að nota Microsoft Power BI áður en hægt er að læra meira um það á við [með Leiðsögn Nám síðu fyrir Power BI](https://powerbi.microsoft.com/en-us/guided-learning/?WT.mc_id=PBIService_GetData). Skýrslur sem eru hafðar með í innihald þjónustupakka með bæði ritum og töflur sem innihalda viðbótarupplýsingar. Eftirfarandi tafla lýsir skýrslunum.

| Skýrsla                            | Innihald                                               |
|-----------------------------------|--------------------------------------------------------|
| Hæfni & Greiningu á Þróun | Meðlimur hæfni hópgerðir og hóps stak hæfni eftir gerð |
| Hæfniforstillingu                     | Hæfniforstillingu fyrir valinn starfsmann                |
| Hæfnigreining                    | Hæfni eftir tegund og einkunn                              |

Hægt er að sía gröf og reitir á þessar skýrslur og festa gröf og reitir í í mælaborð. Sjá frekari upplýsingar um hvernig á að sía og pin-númer í Power BI [Stofna og Skilgreina A Mælaborð](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="understanding-the-data-model-and-entities"></a>Skilja gagnalíkan og einingar
Dynamics 365 fyrir Aðgerðir er notuð til að fylla út skýrslur á Hæfni Starfsmanna og Þróun innihald þjónustupakka. Eftirfarandi tafla sýnir einingar sem innihald þjónustupakka var byggð á.

| Eining                            | Innihald                                                                                                   | Tengsl við aðrar einingar                                                                                                                                                                                                                                                                       |
|-----------------------------------|------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Vinnuafls\_CalendarOffset         | Dagatal mótfærir slice skýrslurnar                                                                          |                                                                                                                                                                                                                                                                                                         |
| Vinnuafls\_Fyrirtækis                | Fyrirtæki til að sía skýrslur með                                                                             |                                                                                                                                                                                                                                                                                                         |
| Vinnuafls\_Launa           | Launataxta og tíðni yfir tíma                                                                           |                                                                                                                                                                                                                                                                                                         |
| Vinnuafls\_CurrentCompensation    | Launataxta og tíðni núverandi dagsetningar                                                              | Vinnuafls\_Fyrirtæki Vinnuafls\_CurrentCompensation Vinnuafls\_Lýðfræði Vinnuafls\_Vinnslu Vinnuafls\_Stöðu                                                                                                                                                                                            |
| Vinnuafls\_CurrentPosition        | Stöður frá og með núverandi dagsetningu, jafngildi fulls starfs (FTE), opnar stöður og opna-til-fylla út stöður | Vinnuafls\_Vinnslu Vinnuafls\_Stöðu                                                                                                                                                                                                                                                                      |
| Vinnuafls\_CurrentWorker          | Starfsmenn frá gildandi dagsetningu, aldur og starfsmannafjöldi                                                         | Vinnuafls\_Fyrirtæki Vinnuafls\_Uppbót Vinnuafls\_GeographicLocation Vinnuafls\_Afköst Vinnuafls\_PersonSkill Vinnuafls\_WorkerName Vinnuafls\_ReportsToWorkerName Vinnuafls\_WorkerTitle Vinnuafls\_Lýðfræði Vinnuafls\_Vinnslu Vinnuafls\_Ráðningu Vinnuafls\_Stöðunni                     |
| Vinnuafls\_Dagsetningu                   | Dagar, vikur, mánuðir og ár                                                                             |                                                                                                                                                                                                                                                                                                         |
| Vinnuafls\_Lýðfræði           | Dagsetning fæðingardag kyn, þjóðernisuppruna og hjúskaparstöðu                                                   |                                                                                                                                                                                                                                                                                                         |
| Vinnuafls\_Ráðningu             | Upphafsdagsetningu, lokadagsetningu og dagsetningu umreiknings                                                                  |                                                                                                                                                                                                                                                                                                         |
| Vinnuafls\_GeographicLocation     | Borg, póstnúmer, sýsla kóða og ríki eða hérað                                                           |                                                                                                                                                                                                                                                                                                         |
| Vinnuafls\_Vinnslu                    | Aðgerð, gerð og titil                                                                                  |                                                                                                                                                                                                                                                                                                         |
| Vinnuafls\_JobPreferredSkill      | Stig mikilvægi einkunn, hæfni og hæfni                                                                 | Vinnuafls\_Hæfni Vinnuafls\_Vinnslu                                                                                                                                                                                                                                                                         |
| Vinnuafls\_PastPositionAssignment | Ástæða úthlutun upphafsdagsetningu, lokadagsetningu og vinnslu                                                           | Vinnuafls\_ClaendarOffset Vinnuafls\_Dagsetning Vinnuafls\_Vinnslu Vinnuafls\_Stöðu                                                                                                                                                                                                                            |
| Vinnuafls\_Afköst            | Einkunn, lýsingu og einkunnalíkan                                                                      |                                                                                                                                                                                                                                                                                                         |
| Vinnuafls\_PersonSkill            | Stig dagsetningu stigs og hæfni                                                                               | Vinnuafls\_Hæfni                                                                                                                                                                                                                                                                                        |
| Vinnuafls\_PersonSkillAnalysis    | Dagsetning vottuð, stig, stig og hæfni                                                                    | Vinnuafls\_WorkerName Vinnuafls\_Hæfni                                                                                                                                                                                                                                                                  |
| Vinnuafls\_Stöðu               | Deild FTE, stöðu, stöðugerð og titil                                                        |                                                                                                                                                                                                                                                                                                         |
| Vinnuafls\_PositionTrend          | Stöður yfir tíma FTE og vinnslu                                                                          | Vinnuafls\_CalendarOffset Vinnuafls\_Dagsetning Vinnuafls\_Vinnslu Vinnuafls\_Stöðu                                                                                                                                                                                                                            |
| Vinnuafls\_ReportsToWorkerName    | Fornafn eftirnafn og fullt nafn                                                                       |                                                                                                                                                                                                                                                                                                         |
| Vinnuafls\_Hæfni                  | Hæfni, gerð hæfni og einkunn                                                                              |                                                                                                                                                                                                                                                                                                         |
| Vinnuafls\_TerminatedWorker       | Starfslok starfsmanna starfslokadagur, titli, stöðu og starfi                                             | Vinnuafls\_Fyrirtæki Vinnuafls\_Uppbót Vinnuafls\_GeographicLocation Vinnuafls\_Afköst Vinnuafls\_WorkerName Vinnuafls\_ReportsToWorkerName Vinnuafls\_CalendarOffset Workforces\_Dagsetning Vinnuafls\_WorkerTitle Vinnuafls\_Lýðfræði Vinnuafls\_Ráðningu Vinnuafls\_Vinnslu Vinnuafls\_Stöðunni |
| Vinnuafls\_WorkerName             | Fornafn eftirnafn og fullt nafn                                                                       |                                                                                                                                                                                                                                                                                                         |
| Vinnuafls\_WorkerTitle            | Titill og starfsaldur                                                                                   |                                                                                                                                                                                                                                                                                                         |
| Workorce\_WorkerTrend             | Starfsmenn yfir tíma, starfsmannafjöldi, fyrirtæki og stöðu                                                        | Vinnuafls\_Fyrirtæki Vinnuafls\_Uppbót Vinnuafls\_GeographicLocation Vinnuafls\_Afköst Vinnuafls\_WorkerName Vinnuafls\_ReportsToWorkerName Vinnuafls\_CalendarOffset Workforces\_Dagsetning Vinnuafls\_WorkerTitle Vinnuafls\_Lýðfræði Vinnuafls\_Ráðningu Vinnuafls\_Vinnslu                     |

Þessar einingar voru notaðar til að stofna reiknaðar mælieiningar í gagnalíkani. Þessar reiknaðar mælieiningar eru notaðar til að reikna út afkastavísar (Afkastavísa) og skýrslur sem eru notaðar í innihald þjónustupakka. Ef óskað er að taka með viðbótarútreikning á skýrslur- og mælaborð hægt að sækja og breyta skrá CompetenciesandDevelopment.pbix úr LCS. Þessi skrá er gagnalíkan sjálfgefna sem var notað til að stofna innihald þjónustupakka. Eftir breytingar, hægt er að stofna til fyrirtækis innihald þjónustupakka og mælaborð sem innihalda upplýsingar sem hefur verið bætt við.

## <a name="additional-resources"></a>Frekari upplýsingar
Hér eru gagnlegir tenglar sem tengjast einingar og að búa til Power BI-efni:

-   [Gagnaeiningar](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/)
-   [Stofnun efnispakka fyrirtækis ](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   [Gera gagnalíkön með því að nota Power BI](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [Bæta Power BI-reitum við vinnusvæði](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/07/06/pinning-power-bi-reports-to-dynamics-ax-client/)



