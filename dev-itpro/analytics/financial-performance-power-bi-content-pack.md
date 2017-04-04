---
title: "Fjárhagsleg Afköst Power BI efni"
description: "Þetta efnisatriði lýsir Microsoft Dynamics 365 fyrir Aðgerðir Fjárhagslega Frammistöðu innihaldi pakka fyrir Microsoft Power BI. Það lýsir mælaborð og skýrslur sem eru hafðar með í innihald þjónustupakka og upplýsingar um gagnalíkan og einingar sem voru notaðir til að búa til innihald þjónustupakka."
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

# <a name="financial-performance-power-bi-content"></a>Fjárhagsleg Afköst Power BI efni

Þetta efnisatriði lýsir Microsoft Dynamics 365 fyrir Aðgerðir Fjárhagslega Frammistöðu innihaldi pakka fyrir Microsoft Power BI. Það lýsir mælaborð og skýrslur sem eru hafðar með í innihald þjónustupakka og upplýsingar um gagnalíkan og einingar sem voru notaðir til að búa til innihald þjónustupakka.

<a name="accessing-the-content-pack"></a>Fara í hugbúnaðarhlutartréð innihaldi pakka
--------------------------

Tvær útgáfur innihald þjónustupakka Fjárhagsleg Afköst eru tiltækar. Ein útgáfa er tiltæk úr Microsoft Dynamics Lifecycle Services (LCS) og aðrar er tiltækt frá PowerBI.com.

-   **Útgáfa sem er tiltæk úr LCS:** í Fjárhagslega Frammistöðu innihaldi pakka sem er tiltæk úr LCS styður Microsoft Dynamics 365 Aðgerðir útgáfu 1611. Hægt er að finna innihald þjónustupakka í Samnýttum eignasafni í LCS. Nánari upplýsingar um hvernig á að sækja innihald þjónustupakka og tengja hana við Microsoft Dynamics 365 fyrir Aðgerðir í [Power BI efni í LCS frá Microsoft og for your viðskiptaaðila](power-bi-content-microsoft-partners.md).
-   **Útgáfa sem er tiltæk úr PowerBI.com:** í Fjárhagslega Frammistöðu innihaldi pakka sem er tiltæk úr PowerBI.com styður Microsoft Dynamics AX útgáfur 7,0 og 7.0.1. Nánari upplýsingar um hvernig á að tengjast og sækja skal Dynamics 365 fyrir Aðgerðir í [Aðgang Power BI efni úr PowerBI.com](power-bi-home-page.md).

## <a name="main-account-setup"></a>Uppsetning aðallykils
Þar sem fyrirtæki á skuldir og tekjuupphæðir birtist sem jákvætt upphæðir í skýrslum, er mikilvægt uppsetningu aðallykla í Dynamics 365 fyrir Aðgerðir. Fyrir þessar aðallykla til að birtast sem jákvætt upphæðir, aðallykilgerðin verður stillt á **Skuld** eða **Tekjur**. Þegar þessar gerðir lykla eru notaðar skýrslur með Microsoft Power BI verður snúa á formerki og sýna upphæðir sem jákvætt.

## <a name="dashboard-and-reports-that-are-included-in-the-content-pack"></a>Mælaborð og skýrslur sem eru hafðar með í innihald þjónustupakka
Eftir að þú hefur tengt Efnispakka við gögn Dynamics 365 for Operations, sýna mælaborð og skýrslur fjárhagsleg gögn þín. Ef aldrei hefur verið að nota Power BI áður en hægt er að læra meira um það á við [með Leiðsögn Nám síðu fyrir Power BI](https://powerbi.microsoft.com/en-us/guided-learning/?WT.mc_id=PBIService_GetData). Mælaborð inniheldur samantekna gagnareiti sem byggjast á undirliggjandi skýrslum. Hver reitur inniheldur samanteknar upplýsingar fyrir núverandi ár yfir öll fyrirtæki í samstæðu. Hér eru sum á reitir:

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

Hver reitar er að afrita eftir supporting skýrslu. Þessar skýrslur innihalda bæði gröf og töflur sem veita frekari upplýsingar. Eftirfarandi tafla lýsir skýrslunum.

| Skýrsla                      | Í skýrslunni koma fram eftirfarandi upplýsingar:                                                                                                                                                                                                                                                                                                          |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Greining reiðufés               | Reiðufé eftir lögaðila reiðufé eftir fjórðungi, samtals reiðufjár og reiðufé eftir **Athugasemd:** á **Reiðufé eftir ársfjórðungum** skýrsla ekki hafa upphafsstöður í samtölu fyrir fyrsta ársfjórðung. Hún sýnir heildarupphæð nýjar færslur sem bókaðar eru á hverjum ársfjórðungi.                                                                                |
| Greining veltufjárhlutfalls      | Veltufjárhlutfall eftir lögaðila, veltufjárhlutfall eftir ársfjórðungi, og stöður fyrir veltufjármuni og skammtímaskuldir                                                                                                                                                                                                                              |
| Greining lausafjárhlutfalls        | Flýtihlutfall eftir lögaðila, flýtihlutfall eftir fjórðungi og stöður fyrir staðgreiðsluafslátt, lykla viðskiptavina og núverandi skuldir                                                                                                                                                                                                                      |
| Greining kostnaður seldra vara | Kostnaður seldra vara (COGS) eftir lögaðila, kostnaður seldra vara þessa árs og síðasta árs eftir ársfjórðungi, COGS gagnvart sölu eftir lögaðila, heildar COGS, og COGS gagnvart söluhlutfalli.                                                                                                                                                                                   |
| Greining veltufés    | Veltufé eftir lögaðila, veltufé eftir ársfjórðungi, veltufjármunir, skammtímaskuldir, og heildar veltufé.                                                                                                                                                                                                                   |
| Greining eigna og skulda     | Ávöxtun heildareigna og skuldir gagnvart heildareignum eftir lögaðila, skuld gagnvart heildareignum og ávöxtun heildareigna yfirstandandi ársfjórðungs, eignir og skuldir.                                                                                                                                                                                     |
| Greining hagnaðarhlutfalls      | Raunverulegt og áætlað hagnaðarhlutfall eftir lögaðila, hagnaðarhlutfall eftir ársfjórðingi, prósenta hagnaðarhlutfalls, og hagnaðarhlutfall.                                                                                                                                                                                                                       |
| Greining hreinna tekja         | Raunverulegar á áætlaðar hreinar tekjur eftir lögaðila, hreinar tekjur þessa og síðasta árs og útgjöld gagnvart prósentu hreinna tekja                                                                                                                                                                                                                       |
| Greining hagnaðar           | Raunverluegar og áætlaðar tekjur fyrir vexti og skatta (EBIT) eftir lögaðila, Rekstrarhagnaður (EBIT) þessa árs og síðasta árs, útgjöld gagnvart tekjuhlutfalli, og raunverulegur og áætlaðar kostnaðar gagnvart tekjum.                                                                                                                                                          |
| Greining tekja            | Heildartekjur, raunverulegar og áætlaðar heildartekjur eftir lögaðila, heildartekjur þessa árs og síðasta árs, fjárhagsfrávik eftir lögaðila og heildartekjur þessa tímabils og síðasta tímabils.                                                                                                                                                 |
| Greining kostnaðar            | Heildarupphæð kostnaðar, raunveruleg áætlun heildarkostnaðar eftir lögaðila, raunveruleg og áætluð heildarkostnaður eftir ársfjórðingu, heildarútgjöld eftir tegund lykils, og hlutfall rekstrargjalda.                                                                                                                                                                 |
| Greining reikningsfærðra tekja     | Samtala viðskiptakröfur, samtals viðskiptakröfum eftir lögaðila, samtals viðskiptavinir eftir fjórðungi, og stöðu fyrir lykla viðskiptavina lykla **Athugasemd:** skýrslum sem ekki hafa upphafsstöður fyrir fjárhagslykla viðskiptavina. Þær sýna samtals nýjar færslur eru bókaðar í Lykla viðskiptavina. |

Hægt er að sía og festa Gröf og reitir á þessar skýrslur við mælaborð. Nánari upplýsingar um hvernig á að sía og festa í Power BI, sjá [Stofna og Skilgreina Mælaborð](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="understanding-the-data-model-and-entities"></a>Skilja gagnalíkan og einingar
Gögn í fyllir mælaborð og skýrslum í innihald þjónustupakka Fjárhagsleg Afköst eru Dynamics 365 fyrir Aðgerðir. Eftirfarandi einingar voru notaðar sem grunnur fyrir innihald þjónustupakka: **Samjafna gagnaeiningar**

-   **GeneralLedgerActivities** – Þessa einingu birtir stöður fjárhags eftir tegund.
-   **BudgetActivities** – birtir Þessi eining áætlunarstöður eftir tegund.

**Data entities**

-   FiscalCalendars
-   MainAccounts
-   LegalEntities
-   Fjárhagur
-   ChartofAccounts

Þessar einingar voru notaðar til að stofna reiknaðar mælieiningar í gagnalíkani. Reiknaðar mælieiningar eru notaðar til að reikna út afkastavísar (Afkastavísa) og skýrslur sem eru notaðar í innihald þjónustupakka. Að sjálfgefnu kemur efnispakkinn með gögng fyrir síðustu þremur árum og komandi árs. Til að hafa viðbótarútreikning með á skýrslur og mælaborð er hægt að breyta [Microsoft Excel vinnubók](https://mbs.microsoft.com/customersource/global/AX/downloads/reports/msdaxfinpercontentpowerbi). Þessi vinnubók er sjálfgefið gagnalíkan sem var notað til að stofna efnispakkann. Eftir að lokið hefur verið gera breytingarnar er hægt að stofna efnispakka fyrirtækis og mælaborð sem innihalda upplýsingar sem hefur verið bætt við.

## <a name="additional-resources"></a>Frekari upplýsingar
Hér eru gagnlegir tenglar sem tengjast einingar og að búa til Power BI-efni:

-   [Gagnaeiningar](..\data-entities\data-entities.md)
-   [Stofnun efnispakka fyrirtækis ](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   [Gera gagnalíkön með því að nota Power BI](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [Bæta Power BI-reitum við vinnusvæði](configure-power-bi-integration.md)



