---
title: "Efni fyrirtækis Þjálfun Power BI"
description: "Þetta efnisatriði lýsir Dynamics 365 aðgerða - Fyrirtækis Þjálfun Power BI efni. Það útskýrt hvernig innihaldi pakka og lýsir gagnalíkan og einingar sem voru notaðir til að búa til innihald þjónustupakka."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: Operations
ms.custom: 263874
ms.assetid: 45dbba14-aba6-4571-be0d-5d1aba3515d9
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 388b6398488e6f316c1ec07a00182e81c1dc8d08
ms.openlocfilehash: 104164f8ffd0d2bc3a64bf15d2fb5213234046ce
ms.lasthandoff: 03/31/2017


---

# <a name="organizational-training-power-bi-content"></a>Efni fyrirtækis Þjálfun Power BI

Þetta efnisatriði lýsir Dynamics 365 aðgerða - Fyrirtækis Þjálfun Power BI efni. Það útskýrt hvernig innihaldi pakka og lýsir gagnalíkan og einingar sem voru notaðir til að búa til innihald þjónustupakka.

<a name="accessing-the-content-pack"></a>Fara í hugbúnaðarhlutartréð innihaldi pakka
--------------------------

Hægt er að finna innihald þjónustupakka Þjálfun Fyrirtækis í eignir safn Samnýttum í Microsoft Dynamics Lifecycle Services (LCS). Nánari upplýsingar um hvernig á að sækja innihald þjónustupakka og tengja hana við Microsoft Dynamics 365 fyrir Aðgerðir í [Power BI efni í LCS frá Microsoft og for your viðskiptaaðila](power-bi-content-microsoft-partners.md).

## <a name="reports-that-are-included-in-the-content-pack"></a>Skýrslur sem eru hafðar með í innihald þjónustupakka
Eftir að þú hefur verið tengdur innihald þjónustupakka skal Dynamics 365 fyrir Aðgerðir, skýrslur sem sýna gögn fyrirtækisins. Ef aldrei hefur verið að nota Microsoft Power BI áður en hægt er að læra meira um það á við [með Leiðsögn Nám síðu fyrir Power BI](https://powerbi.microsoft.com/en-us/guided-learning/?WT.mc_id=PBIService_GetData). Skýrslur sem eru hafðar með í innihald þjónustupakka með bæði ritum og töflur sem innihalda viðbótarupplýsingar. Eftirfarandi tafla lýsir skýrslunum.

| Skýrsla          | Innihald                                                                    |
|-----------------|-----------------------------------------------------------------------------|
| Greining á námskeiði | Skráning eftir staðsetningu, þátttakendur í námskeiði með stöðu og skráningarlisti |
| Námskeiðsgerðir    | Námskeiðsgerðir eftir hæfni                                                       |

Hægt er að sía gröf og reitir á þessar skýrslur og festa gröf og reitir í í mælaborð. Sjá frekari upplýsingar um hvernig á að sía og pin-númer í Power BI [Stofna og Skilgreina A Mælaborð](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="understanding-the-data-model-and-entities"></a>Skilja gagnalíkan og einingar
Dynamics 365 fyrir Aðgerðir er notuð til að fylla út skýrslur í Fyrirtækis Þjálfun innihald þjónustupakka. Eftirfarandi tafla sýnir einingar sem innihald þjónustupakka var byggð á.

| Eining                    | Innihald                                                         | Tengsl við aðrar einingar                                                                                                                                                                  |
|---------------------------|------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Þjálfun\_CalendarOffset  | Dagatal mótfærir slice skýrslurnar                                | Þjálfun\_CourseAgenda Þjálfun\_CourseAttendees                                                                                                                                                   |
| Hjálpargögnum\_Fyrirtækis         | Fyrirtæki til að sía skýrslur með                                   | Þjálfun\_CourseAgenda Þjálfun\_CourseAttendees                                                                                                                                                   |
| Þjálfun\_Námskeiðs          | Námskeið, lýsingu, heiti leiðbeinanda, staðsetningu, plássi og stöðu | Hjálpargögnum\_CourseAgenda Þjálfun\_CourseAttendees Þjálfun\_CourseSkill                                                                                                                             |
| Hjálpargögnum\_CourseAgenda    | Dagskrá námskeiðs og upphafs-og lokatíma                          | Þjálfun\_Fyrirtækis Þjálfun\_CalendarOffset Þjálfun\_Dagsetning Þjálfun\_Námskeiðs                                                                                                                         |
| Þjálfun\_CourseAttendees | Heiti, stöðu, vinnslu og skráningu                         | Þjálfun\_Fyrirtæki Þjálfun\_CalendarOffset Þjálfun\_Dagsetning Þjálfun\_Lýðfræði Þjálfun\_Ráðningu Þjálfun\_Námskeið Þjálfun\_WorkerName Þjálfun\_WorkerTitle Þjálfun\_Vinnslu Þjálfun\_Stöðu |
| Þjálfun\_CourseSkill     | Hæfni, gerð hæfni og stig                                     | Þjálfun\_Námskeiðs                                                                                                                                                                                   |
| Þjálfun\_Dagsetningu            | Dagar, vikur, mánuðir og ár                                   | Þjálfun\_CourseAgenda Þjálfun\_CourseAttendees                                                                                                                                                   |
| Þjálfun\_Lýðfræði    | Dagsetning fæðingardag kyn, þjóðernisuppruna og hjúskaparstöðu         | Þjálfun\_CourseAgenda Þjálfun\_CourseAttendees                                                                                                                                                   |
| Þjálfun\_Starfsráðningu      | Upphafsdagsetningu, lokadagsetningu og dagsetningu umreiknings                        | Þjálfun\_CourseAgenda Þjálfun\_CourseAttendees                                                                                                                                                   |
| Þjálfun\_Vinnslu             | Aðgerð, gerð og titil                                        | Þjálfun\_CourseAgenda Þjálfun\_CourseAttendees                                                                                                                                                   |
| Þjálfun\_Stöðu        | Stöðu, titill og jafngildi fulls starfs (FTE)                  | Þjálfun\_CourseAgenda Þjálfun\_CourseAttendees                                                                                                                                                   |
| Þjálfun\_WorkerName      | Fornafn eftirnafn og fullt nafn                             | Þjálfun\_CourseAttendees                                                                                                                                                                          |
| Hjálpargögnum\_WorkerTitle     | Titill og starfsaldur                                         | Þjálfun\_CourseAttendees                                                                                                                                                                          |

Þessar einingar voru notaðar til að stofna reiknaðar mælieiningar í gagnalíkani. Þessar reiknaðar mælieiningar eru notaðar til að reikna út afkastavísar (Afkastavísa) og skýrslur sem eru notaðar í innihald þjónustupakka. Eigi að taka með viðbótarútreikning skal skýrslur og mælaborð er hægt að sækja og breyta skrá Training.pbix úr LCS. Þessi skrá er gagnalíkan sjálfgefna sem var notað til að stofna innihald þjónustupakka. Eftir breytingar, hægt er að stofna til fyrirtækis innihald þjónustupakka og mælaborð sem innihalda upplýsingar sem hefur verið bætt við.

## <a name="additional-resources"></a>Frekari upplýsingar
Hér eru gagnlegir tenglar sem tengjast einingar og að búa til Power BI-efni:

-   [Gagnaeiningar](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/)
-   [Stofnun efnispakka fyrirtækis ](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   [Gera gagnalíkön með því að nota Power BI](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [Bæta Power BI-reitum við vinnusvæði](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/07/06/pinning-power-bi-reports-to-dynamics-ax-client/)



