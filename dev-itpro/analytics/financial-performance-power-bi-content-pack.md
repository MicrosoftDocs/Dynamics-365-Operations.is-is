---
title: "Power BI-efni fjárhagslegrar frammistöðu"
description: "Þessi efnisgrein skýrir Microsoft Dynamics 365 for Operations efnispakka fyrir Fjárhagsleg frammistaða fyrir Microsoft Power BI. Það lýsir yfirlit og skýrslur sem eru hafðar með í efnispakkanum, og veitir upplýsingar um gagnalíkan og einingar sem voru notaðar til að búa til efnispakka."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 106233
ms.assetid: 517e6a88-e7a1-4398-9971-b22fa83306ba
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 388b6398488e6f316c1ec07a00182e81c1dc8d08
ms.openlocfilehash: 227285720e7f28beeb135eea081940578531d458
ms.lasthandoff: 03/31/2017


---

# <a name="financial-performance-power-bi-content"></a>Power BI-efni fjárhagslegrar frammistöðu

[!include[banner](../includes/banner.md)]


Þessi efnisgrein skýrir Microsoft Dynamics 365 for Operations efnispakka fyrir Fjárhagsleg frammistaða fyrir Microsoft Power BI. Það lýsir yfirlit og skýrslur sem eru hafðar með í efnispakkanum, og veitir upplýsingar um gagnalíkan og einingar sem voru notaðar til að búa til efnispakka.

<a name="accessing-the-content-pack"></a>Farið í efnispakkann
--------------------------

Tvær útgáfur af Efnispakki fyrir Fjárhagsleg frammistaða eru tiltækt. Ein útgáfa tiltæk frá Microsoft Dynamics Lifecycle Services (LCS), og önnur frá PowerBI.com.

-   **Útgáfa sem er tiltækt frá LCS:** Efnispakkinn Fjárhagsleg frammistaða sem er tiltækt frá LCS styður Microsoft Dynamics 365 for Operations útgáfa 1611. Hægt er að finna efnispakka í safninu Samnýttar eignar í LCS. Upplýsingar um hvernig á að sækja efnispakkann og tengja hann við gögn Microsoft Dynamics 365 for Operations er að finna í [Power BI-efni í LCS frá Microsoft og viðskiptaaðilum þínum](power-bi-content-microsoft-partners.md).
-   **Útgáfa sem er tiltæk á PowerBI.com:** Efnispakkinn Fjárhagsleg frammistaða sem er tiltækur á PowerBI.com styður Microsoft Dynamics AX útgáfur 7.0 og 7.0.1. Nánari upplýsingar um hvernig á að tengja og hlaða gögn Microsoft Dynamics 365 for Operations, sjá [Aðgangur Power BI efni úr PowerBI.com](power-bi-home-page.md).

## <a name="main-account-setup"></a>Uppsetning aðallykils
Þar sem fyrr vilja upphæðir skulda og tekjur að birtast sem jákvætt upphæðir í skýrslur er mikilvægt að uppsetning aðallykla í Dynamics 365 for Operations. Til að þessir aðallyklar birtast sem jákvætt upphæðir verður aðallykilgerð að vera stillt á **Skuldir** eða **Tekjur**. Þegar þessar gerð lykils er notað verður skýrslugerð í gegnum Microsoft Power BI snúa við merkjum og sýna upphæðir sem jákvætt.

## <a name="dashboard-and-reports-that-are-included-in-the-content-pack"></a>Yfirlit og skýrslur sem eru hafðar með í efnispakka
Eftir að þú hefur tengt Efnispakka við gögn Dynamics 365 for Operations, sýna mælaborð og skýrslur fjárhagsleg gögn þín. Ef þú hefur aldrei áður notað Power BI, má fræðast nánar um það á síðunni [Leiðsögn fyrir Nám fyrir Power BI](https://powerbi.microsoft.com/en-us/guided-learning/?WT.mc_id=PBIService_GetData). Mælaborð inniheldur samantekna gagnareiti sem byggjast á undirliggjandi skýrslum. Hver reitur inniheldur samanteknar upplýsingar fyrir núverandi ár yfir öll fyrirtæki í samstæðu. Hér eru sum af reitir:

-   Innlausn
-   Heildartekjur á þessu ári
-   Heildarkostnaður á þessu ári
-   Nettótekjur þessa árs
-   Lausafjárhlutfall
-   Heildarkostnaður á þessu ári eftir tegund
-   Veltufjárhlutfall
-   Skuld heildareigna
-   Raunverulegt miðað við spáðar Tekjur
-   Reikningsfærðar tekjur á þessu ári
-   Hlutfall rekstrargjalda á þessu ári
-   Hagnaðarhlutfall þessa árs
-   Rauntölur kostnaðar samanb. v. áætlun - öll fyrirtæki

Hver reitir fá stuðning frá skýrslu. Þessar skýrslur innihalda bæði gröf og töflur sem veita frekari upplýsingar. Eftirfarandi tafla lýsir skýrslunum.

| Skýrsla                      | Í skýrslunni koma fram eftirfarandi upplýsingar:                                                                                                                                                                                                                                                                                                          |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Greining reiðufés               | Reiðufé eftir lögaðila, reiðufé eftir fjórðungi, samtals reiðufé, og reiðufé eftir lyklum **Athugasemd:** Skýrslan **Reiðufé eftir fjórðungi** inniheldur ekki upphafsstöðu í samtölu fyrir fyrsta fjórðung. Hún sýnir samtala nýrra færsla sem er bóka í hverjum fjórðungi.                                                                                |
| Greining veltufjárhlutfalls      | Veltufjárhlutfall eftir lögaðila, veltufjárhlutfall eftir ársfjórðungi, og stöður fyrir veltufjármuni og skammtímaskuldir                                                                                                                                                                                                                              |
| Greining lausafjárhlutfalls        | Lausafjárhlutfall eftir lögaðila, lausafjárhlutfall eftir ársfjórðungi, og stöður fyrir reiðufé, viðskiptakröfur og skammtímaskuldir                                                                                                                                                                                                                      |
| Greining kostnaður seldra vara | Kostnaður seldra vara (COGS) eftir lögaðila, kostnaður seldra vara þessa árs og síðasta árs eftir ársfjórðungi, COGS gagnvart sölu eftir lögaðila, heildar COGS, og COGS gagnvart söluhlutfalli.                                                                                                                                                                                   |
| Greining veltufés    | Veltufé eftir lögaðila, veltufé eftir ársfjórðungi, veltufjármunir, skammtímaskuldir, og heildar veltufé.                                                                                                                                                                                                                   |
| Greining eigna og skulda     | Ávöxtun heildareigna og skuldir gagnvart heildareignum eftir lögaðila, skuld gagnvart heildareignum og ávöxtun heildareigna yfirstandandi ársfjórðungs, eignir og skuldir.                                                                                                                                                                                     |
| Greining hagnaðarhlutfalls      | Raunverulegt og áætlað hagnaðarhlutfall eftir lögaðila, hagnaðarhlutfall eftir ársfjórðingi, prósenta hagnaðarhlutfalls, og hagnaðarhlutfall.                                                                                                                                                                                                                       |
| Greining hreinna tekja         | Raunverulegar á áætlaðar hreinar tekjur eftir lögaðila, hreinar tekjur þessa og síðasta árs og útgjöld gagnvart prósentu hreinna tekja                                                                                                                                                                                                                       |
| Greining hagnaðar           | Raunverluegar og áætlaðar tekjur fyrir vexti og skatta (EBIT) eftir lögaðila, Rekstrarhagnaður (EBIT) þessa árs og síðasta árs, útgjöld gagnvart tekjuhlutfalli, og raunverulegur og áætlaðar kostnaðar gagnvart tekjum.                                                                                                                                                          |
| Greining tekja            | Heildartekjur, raunverulegar og áætlaðar heildartekjur eftir lögaðila, heildartekjur þessa árs og síðasta árs, fjárhagsfrávik eftir lögaðila og heildartekjur þessa tímabils og síðasta tímabils.                                                                                                                                                 |
| Greining kostnaðar            | Heildarupphæð kostnaðar, raunveruleg áætlun heildarkostnaðar eftir lögaðila, raunveruleg og áætluð heildarkostnaður eftir ársfjórðingu, heildarútgjöld eftir tegund lykils, og hlutfall rekstrargjalda.                                                                                                                                                                 |
| Greining reikningsfærðra tekja     | Heildarviðskiptakröfur, heildarviðskiptakröfur eftir lögaðila, heildarviðskiptakröfur eftir ársfjórðungi, og stöður fyrir lykla viðskiptakrafna **Athugasemd:** Skýrslurnar innihalda ekki upphafsstaða fyrir fjárhagslykla viðskiptakröfur. Þær sýnir samtala nýrra færsla sem er bóka viðskiptakröfur. |

Hægt er að sía og festa Gröf og reitir á þessar skýrslur við mælaborð. Nánari upplýsingar um hvernig á að sía og festa í Power BI, sjá [Stofna og Skilgreina Mælaborð](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="understanding-the-data-model-and-entities"></a>Skilja gagnalíkan og einingar
Gögn sem er notuð til að fylla út yfirlit og skýrslum í Efnispakka fjárhagslegrar frammistöðu er gögn Dynamics 365 for Operations. Eftirfarandi einingar voru notaðar sem grunnur að efnispakka: **Einingar uppsafnaðra gagna**

-   **GeneralLedgerActivities** – Þessi eining leggur saman fjárhagsstöður eftir tegund lykla.
-   **BudgetActivities** – Þessi eining leggur saman staða fjárhagsáætlunar eftir tegund lykla.

**Gagnaeiningar**

-   FiscalCalendars
-   MainAccounts
-   LegalEntities
-   Fjárhagur
-   ChartofAccounts

Þessar einingar voru notaðar til að stofna reiknaðar mælieiningar í gagnalíkaninu. Þessar reiknuðu mælieiningar eru notaðar til að stofna reiknaðar ráðstafanir til að reikna út afkastavísar (KPI ) og skýrslur sem eru notaðar í efnispakkanum. Að sjálfgefnu kemur efnispakkinn með gögng fyrir síðustu þremur árum og komandi árs. Til að hafa viðbótarútreikning með á skýrslur og mælaborð er hægt að breyta [Microsoft Excel vinnubók](https://mbs.microsoft.com/customersource/global/AX/downloads/reports/msdaxfinpercontentpowerbi). Þessi vinnubók er sjálfgefið gagnalíkan sem var notað til að stofna efnispakkann. Eftir að lokið hefur verið gera breytingarnar er hægt að stofna efnispakka fyrirtækis og mælaborð sem innihalda upplýsingar sem hefur verið bætt við.

## <a name="additional-resources"></a>Frekari upplýsingar
Hér eru gagnlegir tenglar sem tengjast einingar og að búa til Power BI-efni:

-   [Gagnaeiningar](..\data-entities\data-entities.md)
-   [Stofnun efnispakka fyrirtækis ](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   [Gera gagnalíkön með því að nota Power BI](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [Bæta Power BI-reitum við vinnusvæði](configure-power-bi-integration.md)





