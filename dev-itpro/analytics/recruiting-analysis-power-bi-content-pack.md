---
title: "Ráða Power BI-efni"
description: "Þetta efnisatriði lýsir Dynamics 365 aðgerða - Ráða Power BI efni. Það útskýrt hvernig á að fá aðgang að skýrslunum sem eru innifaldar í innihald þjónustupakka og upplýsingar um gagnalíkan og einingar sem voru notaðir til að búa til innihald þjónustupakka."
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
translationtype: Human Translation
ms.sourcegitcommit: 388b6398488e6f316c1ec07a00182e81c1dc8d08
ms.openlocfilehash: d307733193b388149f83dd420cc7003edcf7749a
ms.lasthandoff: 03/31/2017


---

# <a name="recruiting-power-bi-content"></a>Ráða Power BI-efni

Þetta efnisatriði lýsir Dynamics 365 aðgerða - Ráða Power BI efni. Það útskýrt hvernig á að fá aðgang að skýrslunum sem eru innifaldar í innihald þjónustupakka og upplýsingar um gagnalíkan og einingar sem voru notaðir til að búa til innihald þjónustupakka.

<a name="accessing-the-content-pack"></a>Fara í hugbúnaðarhlutartréð innihaldi pakka
--------------------------

Hægt er að finna innihald þjónustupakka Ráðning í Samnýttum eignir safn í Microsoft Dynamics Lifecycle Services (LCS). Nánari upplýsingar um hvernig á að sækja innihald þjónustupakka og tengja hana við Microsoft Dynamics 365 fyrir Aðgerðir í [Power BI efni í LCS frá Microsoft og for your viðskiptaaðila](power-bi-content-microsoft-partners.md).

## <a name="reports-that-are-included-in-the-content-pack"></a>Skýrslur sem eru hafðar með í innihald þjónustupakka
Eftir að þú hefur verið tengdur innihald þjónustupakka skal Dynamics 365 fyrir Aðgerðir, skýrslur sem sýna gögn fyrirtækisins. Ef aldrei hefur verið að nota Microsoft Power BI áður en hægt er að læra meira um það á við [með Leiðsögn Nám síðu fyrir Power BI](https://powerbi.microsoft.com/en-us/guided-learning/?WT.mc_id=PBIService_GetData). Skýrslur sem eru hafðar með í innihald þjónustupakka með bæði ritum og töflur sem innihalda viðbótarupplýsingar. Eftirfarandi tafla lýsir skýrslunum.

| Skýrsla                       | Innihald                                                                                               |
|------------------------------|--------------------------------------------------------------------------------------------------------|
| Greining umsækjanda           | Umsækjendur með vinnslu, uppruna umsækjanda, umsækjendur eftir staðsetningu og heildarfjöldi umsækjenda           |
| Staða umsækjanda             | Umsækjendur með gerð og stöðu og stöðu umsækjanda                                                    |
| Lýðfræði umsækjanda       | Umsækjendur með aldur og kyn og umsækjendur með því að stig menntun og stöðu                             |
| Ráðningar Greiningar          | Nettó hlutfall ráðningarreglu, daga til að ráða, prósentuhlutfall ósamhæft starfsmenn og kostnað ráðningar að meðaltali                    |
| Verk Analysis ráðningarverk | Fjöldi ráðningarverk, auglýstra starfa eftir ráðningarverki og umsækjendur eftir ráðningarverki |

Hægt er að sía gröf og reitir á þessar skýrslur og festa gröf og reitir í í mælaborð. Sjá frekari upplýsingar um hvernig á að sía og pin-númer í Power BI [Stofna og Skilgreina A Mælaborð](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="understanding-the-data-model-and-entities"></a>Skilja gagnalíkan og einingar
Dynamics 365 fyrir Aðgerðir er notuð til að fylla út í skýrslur í Ráðning innihald þjónustupakka. Eftirfarandi tafla sýnir einingar sem innihald þjónustupakka var byggð á.

| Eining                          | Innihald                                                         | Tengsl við aðrar einingar                                                                                                                                                                                                                 |
|---------------------------------|------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Ráða\_Umsækjanda           | Umsækjendur, nettó ráða hlutfall ráðni umsækjendur og kostnað          | Ráða\_ApplicantName Ráða\_Fyrirtæki Ráða\_CalendarOffset Recuriting\_Dagsetning Ráða\_GeographicLocation Ráða\_Lýðfræði Ráða\_Vinnslu Ráða\_Miðla Ráða\_RecruitmentProject                                |
| Ráða\_ApplicantName       | Umsækjandi fornafn eftirnafn og fullt nafn                   | Ráða\_Ráða Umsækjanda\_EmployedApplicant Ráða\_TerminatedApplicant                                                                                                                                                               |
| Ráða\_CalendarOffset      | Dagatal mótfærir slice skýrslurnar                                | Ráða\_Ráða Umsækjanda\_EmployedApplicant Ráða\_TerminatedApplicant                                                                                                                                                               |
| Ráða\_Fyrirtækis             | Fyrirtæki til að sía skýrslur með                                   | Ráða\_Ráða Umsækjanda\_EmployedApplicant Ráða\_TerminatedApplicant                                                                                                                                                               |
| Ráða\_Dagsetningu                | Dagar, vikur, mánuðir og ár                                   | Ráða\_Ráða Umsækjanda\_EmployedApplicant Ráða\_TerminatedApplicant                                                                                                                                                               |
| Ráða\_Lýðfræði        | Dagsetning fæðingardag kyn, þjóðernisuppruna og hjúskaparstöðu         | Ráða\_Ráða Umsækjanda\_EmployedApplicant Ráða\_TerminatedApplicant                                                                                                                                                               |
| Ráða\_EmployedApplicant   | Gerð umsækjanda, afköst, upphafsdagsetningu og umsækjanda           | Ráða\_Fyrirtæki Ráða\_CalendarOffset Ráða\_Dagsetning Ráða\_GeographicLocation Ráða\_ApplicantName Ráða\_Ráðningu Ráða\_Afköst Ráða\_Vinnslu Ráða\_Miðla Ráða\_RecruitmentProject          |
| Ráða\_Ráðningu          | Upphafsdagsetningu, lokadagsetningu og dagsetningu umreiknings                        | Ráða\_Ráða Umsækjanda\_EmployedApplicant Ráða\_TerminatedApplicant                                                                                                                                                               |
| Ráða\_GeographicLocation  | Borg, póstnúmer, sýsla kóða og ríki eða hérað                 | Ráða\_Ráða Umsækjanda\_EmployedApplicant Ráða\_TerminatedApplicant                                                                                                                                                               |
| Ráða\_Vinnslu                 | Aðgerð, gerð og titil                                        | Ráða\_Ráða Umsækjanda\_EmployedApplicant Ráða\_TerminatedApplicant                                                                                                                                                               |
| Ráða\_Miðla               | Uppruni umsækjenda                                             | Ráða\_Ráða Umsækjanda\_EmployedApplicant Ráða\_TerminatedApplicant                                                                                                                                                               |
| Ráða\_Afköst         | Einkunn, lýsingu og einkunnalíkan                            | Ráða\_Ráða Umsækjanda\_EmployedApplicant Ráða\_TerminatedApplicant                                                                                                                                                               |
| Ráða\_RecruitmentProject  | Lýsing á stöðu og auglýstra starfa                | Ráða\_Ráða Umsækjanda\_EmployedApplicant Ráða\_TerminatedApplicant                                                                                                                                                               |
| Ráða\_TerminatedApplicant | Hættur umsækjendur ástæðukóða, afköst og starfslokadagur | Ráða\_Fyrirtæki Ráða\_CalendarOffset Ráða\_Dagsetning Ráða\_GeographicLocation Ráða\_Afköst Ráða\_Lýðfræði Ráða\_Ráðningu Ráða\_Miðla Ráða\_RecruitmentProject Ráða\_ApplicantName |

Þessar einingar voru notaðar til að stofna reiknaðar mælieiningar. Þessar reiknaðar mælieiningar eru notaðar til að reikna út afkastavísar (Afkastavísa) og skýrslur sem eru notaðar í innihald þjónustupakka. Eigi að taka með viðbótarútreikning á skýrslur- og mælaborð er hægt að sækja og breyta skrá Recruiting.pbix úr LCS. Þessi skrá er gagnalíkan sjálfgefna sem var notað til að stofna innihald þjónustupakka. Eftir breytingar, hægt er að stofna til fyrirtækis innihald þjónustupakka og mælaborð sem innihalda upplýsingar sem hefur verið bætt við.

## <a name="additional-resources"></a>Frekari upplýsingar
Hér eru gagnlegir tenglar sem tengjast einingar og að búa til Power BI-efni:

-   [Gagnaeiningar](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/)
-   [Stofnun efnispakka fyrirtækis ](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   [Gera gagnalíkön með því að nota Power BI](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [Bæta Power BI-reitum við vinnusvæði](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/07/06/pinning-power-bi-reports-to-dynamics-ax-client/)



