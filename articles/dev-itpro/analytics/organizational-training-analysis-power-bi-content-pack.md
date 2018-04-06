---
title: "Þjálfun fyrirtækis Power BI-efni"
description: "Þetta efnisatriði lýsir Finance and Operations - Fyrirtækjaþjálfun Power BI efnis."
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
ms.custom: 263874
ms.assetid: 45dbba14-aba6-4571-be0d-5d1aba3515d9
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 19cc8f92b5bb6d9ddfdc77785e48de17ed005703
ms.openlocfilehash: 18567a3241fce02e17df368f544e545fad93e1d9
ms.contentlocale: is-is
ms.lasthandoff: 03/23/2018

---

# <a name="organizational-training-power-bi-content"></a>Þjálfun fyrirtækis Power BI-efni

[!include[banner](../includes/banner.md)]


Þetta efnisatriði lýsir Finance and Operations - Fyrirtækjaþjálfun Power BI efnis. 

## <a name="reports-that-are-included-in-the-content-pack"></a>Skýrslur sem eru hafðar með í efnispakka
Eftir að þú hefur tengt efnispakkann við gögn Finance and Operations sýnir skýrslan þér fyrirtækjagögn þín. Ef þú hefur aldrei áður notað Microsoft Power BI, má fræðast nánar um það á síðunni [Leiðsögn fyrir Nám fyrir Power BI](https://powerbi.microsoft.com/en-us/guided-learning/?WT.mc_id=PBIService_GetData). Skýrslur sem eru hafðar með í efnispakka hafa bæði gröf og töflur sem innihalda viðbótarupplýsingar. Eftirfarandi tafla lýsir skýrslunum.

| Skýrsla          | Innihald                                                                    |
|-----------------|-----------------------------------------------------------------------------|
| Greining á námskeiði | Skráning eftir staðsetningu, þátttakendur í námskeiði eftir stöðu og skráningarlisti |
| Námskeiðsgerðir    | Námskeiðsgerðir eftir hæfni                                                       |

Hægt er að sía gröf og reiti í þessum skýrslum og festa gröf og reiti á yfirlitið. Nánari upplýsingar um hvernig á að sía og festa í Power BI, sjá [Stofna og Skilgreina Mælaborð](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="understanding-the-data-model-and-entities"></a>Skilja gagnalíkan og einingar
Gögn Finance and Operations eru notuð til að fylla út skýrslurnar í efnispakka fyrirtækjaþjálfunar. Eftirfarandi tafla sýnir einingar sem efnispakkinn var byggður á.

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





