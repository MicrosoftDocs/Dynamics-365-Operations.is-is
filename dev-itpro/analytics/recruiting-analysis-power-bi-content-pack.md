---
title: "Ráða Power BI-efni"
description: "Þetta efnisatriði lýsir Dynamics 365 for Operations - Ráða Power BI-efni. Það lýsir einnig hvernig eigi að fara í skýrslur sem eru hafðar með í efnispakkanum, og veitir upplýsingar um gagnalíkan og einingar sem voru notaðar til að búa til efnispakka."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: Operations
ms.custom: 263934
ms.assetid: 38e6827b-0819-473c-bc47-821a1ec482b8
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 15780e7db5867a2f6a484ceb663e617345c033c2
ms.contentlocale: is-is
ms.lasthandoff: 04/25/2017


---

# <a name="recruiting-power-bi-content"></a>Ráða Power BI-efni

[!include[banner](../includes/banner.md)]


Þetta efnisatriði lýsir Dynamics 365 for Operations - Ráða Power BI-efni. Það lýsir einnig hvernig eigi að fara í skýrslur sem eru hafðar með í efnispakkanum, og veitir upplýsingar um gagnalíkan og einingar sem voru notaðar til að búa til efnispakka.

<a name="accessing-the-content-pack"></a>Farið í efnispakkann
--------------------------

Hægt er að finna þjálfunarpakka í safninu Samnýttar eignar í Microsoft Dynamics Lifecycle Services (LCS). Upplýsingar um hvernig á að sækja efnispakkann og tengja hann við gögn Microsoft Dynamics 365 for Operations er að finna í [Power BI-efni í LCS frá Microsoft og viðskiptaaðilum þínum](power-bi-content-microsoft-partners.md).

## <a name="reports-that-are-included-in-the-content-pack"></a>Skýrslur sem eru hafðar með í efnispakka
Eftir að þú hefur tengt efnispakkann við gögn Dynamics 365 for Operations, sýnir skýrslan þér fyrirtækjagögn þín. Ef þú hefur aldrei áður notað Microsoft Power BI, má fræðast nánar um það á síðunni [Leiðsögn fyrir Nám fyrir Power BI](https://powerbi.microsoft.com/en-us/guided-learning/?WT.mc_id=PBIService_GetData). Skýrslur sem eru hafðar með í efnispakka hafa bæði gröf og töflur sem innihalda viðbótarupplýsingar. Eftirfarandi tafla lýsir skýrslunum.

| Skýrsla                       | Innihald                                                                                               |
|------------------------------|--------------------------------------------------------------------------------------------------------|
| Greining umsækjanda           | Umsækjendur eftir verki, uppruna umsækjanda, umsækjendur eftir staðsetningu og heildarfjöldi umsækjenda           |
| Umsækjandastaða             | Umsækjendur eftir gerð og stöðu og stöðu umsækjanda                                                    |
| Lýðfræði umsækjanda       | Umsækjendur eftir aldri og kyni og umsækjendur eftir menntun og stöðu                             |
| Greining ráðninga          | Nettó hlutfall ráðninga, dagar til að ráða, prósentuhlutfall vondra ráðninga og kostnaður ráðninga                    |
| Greining ráðningarverka | Fjöldi ráðningarverka, opnana eftir ráðningarverki og umsækjendur eftir ráðningarverki |

Hægt er að sía gröf og reiti í þessum skýrslum og festa gröf og reiti á yfirlitið. Nánari upplýsingar um hvernig á að sía og festa í Power BI, sjá [Stofna og Skilgreina Mælaborð](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="understanding-the-data-model-and-entities"></a>Skilja gagnalíkan og einingar
Gögn Dynamics 365 for Operations eru notuð til að mynda skýrslunr í efnispakka ráðninga. Eftirfarandi tafla sýnir einingar sem efnispakkinn var byggður á.

| Eining                          | Innihald                                                         | Vensl við aðra lögaðila                                                                                                                                                                                                                 |
|---------------------------------|------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Ráða\_Umsækjanda           | Umsækjendur, ráðnir, ráðningarhlutfall og kostnaður          | Ráðning\_ApplicantName Recruiting\_Company Recruiting\_CalendarOffset Recuriting\_Date Recruiting\_GeographicLocation Recruiting\_Demographics Recruiting\_Job Recruiting\_Media Recruiting\_RecruitmentProject                                |
| Ráðning\_ApplicantName       | Fornanfn umsækjanda, eftirnafn, og fullt nafn                   | Ráðning\_Applicant Recruiting\_EmployedApplicant Recruiting\_TerminatedApplicant                                                                                                                                                               |
| Ráðning\_CalendarOffset      | Mótbókanir dagatals til að sneiða skýrslur                                | Ráðning\_Applicant Recruiting\_EmployedApplicant Recruiting\_TerminatedApplicant                                                                                                                                                               |
| Ráðning\_Company             | Fyrirtæki til að sía skýrsla eftir                                   | Ráðning\_Applicant Recruiting\_EmployedApplicant Recruiting\_TerminatedApplicant                                                                                                                                                               |
| Ráðning\_Date                | Dagar, vikur, mánuðir og ár                                   | Ráðning\_Applicant Recruiting\_EmployedApplicant Recruiting\_TerminatedApplicant                                                                                                                                                               |
| Ráðning\_Demographics        | Fæðingardagur, kyn, þjóðernisuppruni og hjúskapaarstaða         | Ráðning\_Applicant Recruiting\_EmployedApplicant Recruiting\_TerminatedApplicant                                                                                                                                                               |
| Ráðning\_EmployedApplicant   | Umsækjandi, frammistaða, upphafsdagur og gerð umsækjanda           | Ráðning\_Company Recruiting\_CalendarOffset Recruiting\_Date Recruiting\_GeographicLocation Recruiting\_ApplicantName Recruiting\_Employment Recruiting\_Performance Recruiting\_Job Recruiting\_Media Recruiting\_RecruitmentProject          |
| Ráðning\_Employment          | Upphafsdagur, lokadagur og breytingardagur                        | Ráðning\_Applicant Recruiting\_EmployedApplicant Recruiting\_TerminatedApplicant                                                                                                                                                               |
| Ráðning\_GeographicLocation  | Borg, sýsla, póstnúmer og fylki eða Sveitarfélag                 | Ráðning\_Applicant Recruiting\_EmployedApplicant Recruiting\_TerminatedApplicant                                                                                                                                                               |
| Ráðning\_Job                 | Aðgerð, gerð og Titill                                        | Ráðning\_Applicant Recruiting\_EmployedApplicant Recruiting\_TerminatedApplicant                                                                                                                                                               |
| Ráðning\_Media               | Uppruni umsækjanda                                             | Ráðning\_Applicant Recruiting\_EmployedApplicant Recruiting\_TerminatedApplicant                                                                                                                                                               |
| Ráðning\_Performance         | Mat, lýsing og matslíkan                            | Ráðning\_Applicant Recruiting\_EmployedApplicant Recruiting\_TerminatedApplicant                                                                                                                                                               |
| Ráðning\_RecruitmentProject  | Lýsing á verki, staða verks og opnanir                | Ráðning\_Applicant Recruiting\_EmployedApplicant Recruiting\_TerminatedApplicant                                                                                                                                                               |
| Ráðning\_TerminatedApplicant | Umsækendur sem var hafna, ástæða, frammistaða og starfslokadagur | Ráðning\_Company Recruiting\_CalendarOffset Recruiting\_Date Recruiting\_GeographicLocation Recruiting\_Performance Recruiting\_Demographics Recruiting\_Employment Recruiting\_Media Recruiting\_RecruitmentProject Recruiting\_ApplicantName |

Þessar einingar voru notaðar til að stofna reiknaðar mælieiningar. Þessar reikuðu mælieiningar eru síðan notaðar til að stofna reiknaðar ráðstafanir til að reikna út afkastavísar (KPI ) og skýrslur sem eru notaðar í efnispakkanum. Eigi taka á með viðbótarútreikning í skýrslum og mælaborði er hægt að sækja og breyta Recruiting.pbix skrá af LCS. Þessi skrá er sjálfgefið gagnalíkan sem var notað til að stofna efnispakkann. Eftir að breytingarnar hafa verið gerðar er hægt að stofna efnispakka fyrirtækis og mælaborð sem innihalda upplýsingar sem hefur verið bætt við.

## <a name="additional-resources"></a>Frekari upplýsingar
Hér eru gagnlegir tenglar sem tengjast einingar og að búa til Power BI-efni:

-   [Gagnaeiningar](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/)
-   [Stofnun efnispakka fyrirtækis ](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   [Gera gagnalíkön með því að nota Power BI](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [Bæta Power BI-reitum við vinnusvæði](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/07/06/pinning-power-bi-reports-to-dynamics-ax-client/)





