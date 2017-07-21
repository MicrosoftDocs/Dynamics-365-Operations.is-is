---
title: "Fyrirtækjaþjálfun Power BI efni"
description: "Þetta efnisatriði lýsir Finance and Operations - Fyrirtækjaþjálfun Power BI efnis. Það lýsir einnig hvernig eigi að fara í efnispakka, og veitir upplýsingar um gagnalíkan og einingar sem notaðar voru til að búa til efnispakka."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations, UnifiedOperations
ms.custom: 263874
ms.assetid: 45dbba14-aba6-4571-be0d-5d1aba3515d9
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-11-30T00:00:00.000Z
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: 26499bf5423bc3711d110bd7e548eda238162b7a
ms.contentlocale: is-is
ms.lasthandoff: 06/13/2017

---

# <a name="organizational-training-power-bi-content"></a>Fyrirtækjaþjálfun Power BI efni

[!include[banner](../includes/banner.md)]


Þetta efnisatriði lýsir Finance and Operations - Fyrirtækjaþjálfun Power BI efnis. Það lýsir einnig hvernig eigi að fara í efnispakka, og veitir upplýsingar um gagnalíkan og einingar sem notaðar voru til að búa til efnispakka.

<a name="accessing-the-content-pack"></a>Farið í efnispakkann
--------------------------

Hægt er að finna fyrirtækjaþjálfunarpakka í safninu Samnýttar eignir í Microsoft Dynamics Lifecycle Services (LCS). Upplýsingar um hvernig á að sækja efnispakkann og tengja hann við gögn Microsoft Dynamics 365 for Finance and Operations er að finna í [Power BI-efni í LCS frá Microsoft og viðskiptaaðilum þínum](power-bi-content-microsoft-partners.md).

## <a name="reports-that-are-included-in-the-content-pack"></a>Skýrslur sem eru hafðar með í efnispakka
Eftir að þú hefur tengt efnispakkann við gögn Finance and Operations sýnir skýrslan þér fyrirtækjagögn þín. Ef þú hefur aldrei áður notað Microsoft Power BI, má fræðast nánar um það á síðunni [Leiðsögn fyrir Nám fyrir Power BI](https://powerbi.microsoft.com/en-us/guided-learning/?WT.mc_id=PBIService_GetData). Skýrslur sem eru hafðar með í efnispakka hafa bæði gröf og töflur sem innihalda viðbótarupplýsingar. Eftirfarandi tafla lýsir skýrslunum.

| Skýrsla          | Innihald                                                                    |
|-----------------|-----------------------------------------------------------------------------|
| Greining á námskeiði | Skráning eftir staðsetningu, þátttakendur í námskeiði eftir stöðu og skráningarlisti |
| Námskeiðsgerðir    | Námskeiðsgerðir eftir hæfni                                                       |

Hægt er að sía gröf og reiti í þessum skýrslum og festa gröf og reiti á yfirlitið. Nánari upplýsingar um hvernig á að sía og festa í Power BI, sjá [Stofna og Skilgreina Mælaborð](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="understanding-the-data-model-and-entities"></a>Skilja gagnalíkan og einingar
Gögn Finance and Operations eru notuð til að mynda skýrslur í efnispakka fyrirtækjaþjálfunar. Eftirfarandi tafla sýnir einingar sem efnispakkinn var byggður á.

| Eining                    | Innihald                                                         | Vensl við aðra lögaðila                                                                                                                                                                  |
|---------------------------|------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Þjálfun\_CalendarOffset  | Mótbókanir dagatals til að sneiða skýrslur                                | Þjálfun\_CourseAgenda Training\_CourseAttendees                                                                                                                                                   |
| Þjálfun\_Company         | Fyrirtæki til að sía skýrsla eftir                                   | Þjálfun\_CourseAgenda Training\_CourseAttendees                                                                                                                                                   |
| Þjálfun\_Course          | Námskeið, lýsingu, heiti leiðbeinanda, staðsetning, pláss og staða | Þjálfun\_CourseAgenda Training\_CourseAttendees Training\_CourseSkill                                                                                                                             |
| Þjálfun\_CourseAgenda    | Dagskrá, námskeið og upphafs-og lokatími                          | Þjálfun\_Company Training\_CalendarOffset Training\_Date Training\_Course                                                                                                                         |
| Þjálfun\_CourseAttendees | Heiti, staða, vinnslu og skráningardagur                         | Þjálfun\_Company Training\_CalendarOffset Training\_Date Training\_Demographics Training\_Employment Training\_Course Training\_WorkerName Training\_WorkerTitle Training\_Job Training\_Position |
| Þjálfun\_CourseSkill     | Hæfni, gerð hæfni og stig                                     | Þjálfun\_Course                                                                                                                                                                                   |
| Þjálfun\_Date            | Dagar, vikur, mánuðir og ár                                   | Þjálfun\_CourseAgenda Training\_CourseAttendees                                                                                                                                                   |
| Þjálfun\_Demographics    | Fæðingardagur, kyn, þjóðernisuppruni og hjúskapaarstaða         | Þjálfun\_CourseAgenda Training\_CourseAttendees                                                                                                                                                   |
| Þjálfun\_Employment      | Upphafsdagur, lokadagur og breytingardagur                        | Þjálfun\_CourseAgenda Training\_CourseAttendees                                                                                                                                                   |
| Þjálfun\_Job             | Aðgerð, gerð og Titill                                        | Þjálfun\_CourseAgenda Training\_CourseAttendees                                                                                                                                                   |
| Þjálfun\_Position        | Staða, titill og jafngildi fulls starfs (FTE)                  | Þjálfun\_CourseAgenda Training\_CourseAttendees                                                                                                                                                   |
| Þjálfun\_WorkerName      | Fornafn, eftirnafn, og fullt nafn                             | Þjálfun\_CourseAttendees                                                                                                                                                                          |
| Þjálfun\_WorkerTitle     | Titill og starfsaldursdagsetning                                         | Þjálfun\_CourseAttendees                                                                                                                                                                          |

Þessar einingar voru notaðar til að stofna reiknaðar mælieiningar í gagnalíkaninu. Þessar reikuðu mælieiningar eru síðan notaðar til að stofna reiknaðar ráðstafanir til að reikna út afkastavísar (KPI ) og skýrslur sem eru notaðar í efnispakkanum. Eigi taka á með viðbótarútreikning í skýrslum og mælaborði er hægt að sækja og breyta Training.pbix skrá af LCS. Þessi skrá er sjálfgefið gagnalíkan sem var notað til að stofna efnispakkann. Eftir að breytingarnar hafa verið gerðar er hægt að stofna efnispakka fyrirtækis og mælaborð sem innihalda upplýsingar sem hefur verið bætt við.

## <a name="additional-resources"></a>Frekari upplýsingar
Hér eru gagnlegir tenglar sem tengjast einingar og að búa til Power BI-efni:

-   [Gagnaeiningar](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/)
-   [Stofnun efnispakka fyrirtækis ](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   [Gera gagnalíkön með því að nota Power BI](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [Bæta Power BI-reitum við vinnusvæði](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/07/06/pinning-power-bi-reports-to-dynamics-ax-client/)





