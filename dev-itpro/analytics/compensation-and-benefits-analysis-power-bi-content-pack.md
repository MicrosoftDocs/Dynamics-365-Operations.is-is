---
title: "Laun og Fríðindi Power BI efni"
description: "Þetta efnisatriði lýsir Dynamics 365 aðgerða - Laun og Fríðindi Power BI innihald. Það útskýrt hvernig á að fá aðgang að skýrslunum sem eru innifaldar í innihald þjónustupakka og upplýsingar um gagnalíkan og einingar sem voru notaðir til að búa til innihald þjónustupakka."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: Operations
ms.custom: 263914
ms.assetid: 18634bb5-3341-42f2-9cc9-7b04708b506b
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 388b6398488e6f316c1ec07a00182e81c1dc8d08
ms.openlocfilehash: 557f9218032e2b1160b6ea0631ada951353d2afd
ms.lasthandoff: 03/31/2017


---

# <a name="compensation-and-benefits-power-bi-content"></a>Laun og Fríðindi Power BI efni

Þetta efnisatriði lýsir Dynamics 365 aðgerða - Laun og Fríðindi Power BI innihald. Það útskýrt hvernig á að fá aðgang að skýrslunum sem eru innifaldar í innihald þjónustupakka og upplýsingar um gagnalíkan og einingar sem voru notaðir til að búa til innihald þjónustupakka.

<a name="accessing-the-content-pack"></a>Fara í hugbúnaðarhlutartréð innihaldi pakka
--------------------------

Hægt er að finna í Laun og Fríðindi innihald þjónustupakka í Samnýttum eignir safn í Microsoft Dynamics Lifecycle Services (LCS). Nánari upplýsingar um hvernig á að sækja innihald þjónustupakka og tengja hana við Microsoft Dynamics 365 fyrir Aðgerðir í [Power BI efni í LCS frá Microsoft og for your viðskiptaaðila](power-bi-content-microsoft-partners.md).

## <a name="reports-that-are-included-in-the-content-pack"></a>Skýrslur sem eru hafðar með í innihald þjónustupakka
Eftir að þú hefur verið tengdur innihald þjónustupakka skal Dynamics 365 fyrir Aðgerðir, skýrslur sem sýna gögn fyrirtækisins. Ef aldrei hefur verið að nota Microsoft Power BI áður en hægt er að læra meira um það á við [með Leiðsögn Nám síðu fyrir Power BI](https://powerbi.microsoft.com/en-us/guided-learning/?WT.mc_id=PBIService_GetData). Skýrslur sem eru hafðar með í innihald þjónustupakka með bæði ritum og töflur sem innihalda viðbótarupplýsingar. Eftirfarandi tafla lýsir skýrslunum.

| Skýrsla                     | Innihald                                                                                                                              |
|----------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| Comp og Fríðindi Greiningar | Tímakaup og salaried starfsmenn fyrirtæki, meðaltal tímakaup, meðaltal salaried laun starfsmanna eftir atvinnu gerð og áætla innskráningar |
| Fríðindi starfsmanna          | Skráning starfsmanns með völdum fríðindum                                                                                               |

Hægt er að sía gröf og reitir á þessar skýrslur og festa gröf og reitir í í mælaborð. Sjá frekari upplýsingar um hvernig á að sía og pin-númer í Power BI [Stofna og Skilgreina A Mælaborð](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="understanding-the-data-model-and-entities"></a>Skilja gagnalíkan og einingar
Dynamics 365 fyrir Aðgerðir er notuð til að fylla út skýrslur í Laun og Fríðindi innihald pakkanum. Eftirfarandi tafla sýnir einingar sem innihald þjónustupakka var byggð á.

| Eining                            | Innihald                                                                                                   | Tengsl við aðrar einingar                                                                                                                                                                                                                                                                                                |
|-----------------------------------|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Vinnuafls\_CalendarOffset         | Dagatal mótfærir slice skýrslurnar                                                                          | Vinnuafls\_PastPositionAssignment Vinnuafls\_PositionTrend Workorce\_WorkerTrend Vinnuafls\_TerminatedWorker                                                                                                                                                                                                                     |
| Vinnuafls\_Fyrirtækis                | Fyrirtæki til að sía skýrslur með                                                                             | Vinnuafls\_CurrentCompensation Vinnuafls\_CurrentWorker Vinnuafls\_TerminatedWorker Workorce\_WorkerTrend                                                                                                                                                                                                                        |
| Vinnuafls\_Launa           | Launataxta og tíðni yfir tíma                                                                           | Vinnuafls\_CurrentCompensation Vinnuafls\_CurrentWorker Vinnuafls\_TerminatedWorker Workorce\_WorkerTrend                                                                                                                                                                                                                        |
| Vinnuafls\_CurrentCompensation    | Launataxta og tíðni núverandi dagsetningar                                                              | Vinnuafls\_Fyrirtæki Vinnuafls\_Uppbót Vinnuafls\_Lýðfræði Vinnuafls\_Vinnslu Vinnuafls\_Stöðunni                                                                                                                                                                                                                            |
| Vinnuafls\_CurrentPosition        | Stöður frá og með núverandi dagsetningu, jafngildi fulls starfs (FTE), opnar stöður og opna-til-fylla út stöður | Vinnuafls\_Vinnslu Vinnuafls\_Stöðu                                                                                                                                                                                                                                                                                               |
| Vinnuafls\_CurrentWorker          | Starfsmenn frá gildandi dagsetningu, aldur og starfsmannafjöldi                                                         | Vinnuafls\_Fyrirtæki Vinnuafls\_Uppbót Vinnuafls\_GeographicLocation Vinnuafls\_Afköst Vinnuafls\_WorkerName Vinnuafls\_ReportsToWorkerName Vinnuafls\_WorkerTitle Vinnuafls\_Lýðfræði Vinnuafls\_Vinnslu Vinnuafls\_Ráðningu Vinnuafls\_Stöðu Vinnuafls\_WorkerBenefit                                            |
| Vinnuafls\_Dagsetningu                   | Dagar, vikur, mánuðir og ár                                                                             | Vinnuafls\_PastPositionAssignment Vinnuafls\_PositionTrend Vinnuafls\_TerminatedWorker Workorce\_WorkerTrend                                                                                                                                                                                                                     |
| Vinnuafls\_Lýðfræði           | Dagsetning fæðingardag kyn, þjóðernisuppruna og hjúskaparstöðu                                                   | Vinnuafls\_CurrentWorker Vinnuafls\_TerminatedWorker Workorce\_WorkerTrend                                                                                                                                                                                                                                                       |
| Vinnuafls\_Ráðningu             | Upphafsdagsetningu, lokadagsetningu og dagsetningu umreiknings                                                                  | Vinnuafls\_CurrentWorker Vinnuafls\_TerminatedWorker Workorce\_WorkerTrend                                                                                                                                                                                                                                                       |
| Vinnuafls\_GeographicLocation     | Borg, póstnúmer, sýsla kóða og ríki eða hérað                                                           | Vinnuafls\_CurrentWorker Vinnuafls\_TerminatedWorker Workorce\_WorkerTrend                                                                                                                                                                                                                                                       |
| Vinnuafls\_Vinnslu                    | Aðgerð, gerð og titil                                                                                  | Vinnuafls\_CurrentPosition Vinnuafls\_CurrentWorker                                                                                                                                                                                                                                                                              |
| Vinnuafls\_PastPositionAssignment | Ástæða úthlutun upphafsdagsetningu, lokadagsetningu og vinnslu                                                           | Vinnuafls\_CalendarOffset Vinnuafls\_Dagsetning Vinnuafls\_Vinnslu Vinnuafls\_Stöðu                                                                                                                                                                                                                                                     |
| Vinnuafls\_Afköst            | Einkunn, lýsingu og einkunnalíkan                                                                      | Vinnuafls\_CurrentWorker Vinnuafls\_TerminatedWorker Workorce\_WorkerTrend                                                                                                                                                                                                                                                       |
| Vinnuafls\_Stöðu               | Deild FTE, stöðu, stöðugerð og titil                                                        | Vinnuafls\_CurrentPosition Vinnuafls\_CurrentWorker                                                                                                                                                                                                                                                                              |
| Vinnuafls\_PositionTrend          | Stöður yfir tíma FTE og vinnslu                                                                          | Vinnuafls\_CalendarOffset Vinnuafls\_Dagsetning Vinnuafls\_Vinnslu Vinnuafls\_Stöðu                                                                                                                                                                                                                                                     |
| Vinnuafls\_ReportsToWorkerName    | Fornafn eftirnafn og fullt nafn                                                                       | Vinnuafls\_CurrentWorker Vinnuafls\_TerminatedWorker Workorce\_WorkerTrend                                                                                                                                                                                                                                                       |
| Vinnuafls\_Hæfni                  | Hæfni, gerð hæfni og einkunn                                                                              |                                                                                                                                                                                                                                                                                                                                  |
| Vinnuafls\_TerminatedWorker       | Starfslok starfsmanna starfslokadagur, titli, stöðu og starfi                                             | Vinnuafls\_Fyrirtæki Vinnuafls\_Launa Vinnuafls\_GeographicLocation Vinnuafls\_Afköst Vinnuafls\_WorkerName Vinnuafls\_ReportsToWorkerName Vinnuafls\_CalendarOffset Workforces\_Dagsetning Vinnuafls\_WorkerTitle Vinnuafls\_Lýðfræði Vinnuafls\_Ráðningu Vinnuafls\_Vinnslu Vinnuafls\_Stöðu Vinnuafls\_WorkerBenefit |
| Vinnuafls\_WorkerBenefit          | Gildisdagsetning fríðindavalkost, fríðindaáætlun og fríðindagerð                                             | Vinnuafls\_CurrentWorker Vinnuafls\_TerminatedWorker Workorce\_WorkerTrend                                                                                                                                                                                                                                                       |
| Vinnuafls\_WorkerName             | Fornafn eftirnafn og fullt nafn                                                                       | Vinnuafls\_CurrentWorker Vinnuafls\_TerminatedWorker Workorce\_WorkerTrend                                                                                                                                                                                                                                                       |
| Vinnuafls\_WorkerTitle            | Titill og starfsaldur                                                                                   | Vinnuafls\_CurrentWorker Vinnuafls\_TerminatedWorker Workorce\_WorkerTrend                                                                                                                                                                                                                                                       |
| Workorce\_WorkerTrend             | Starfsmenn yfir tíma, starfsmannafjöldi, fyrirtæki og stöðu                                                        | Vinnuafls\_Fyrirtæki Vinnuafls\_Uppbót Vinnuafls\_GeographicLocation Vinnuafls\_Afköst Vinnuafls\_WorkerName Vinnuafls\_ReportsToWorkerName Vinnuafls\_CalendarOffset Workforces\_Dagsetning Vinnuafls\_WorkerTitle Vinnuafls\_Lýðfræði Vinnuafls\_Ráðningu Vinnuafls\_Vinnslu Vinnuafls\_WorkerBenefit                     |

Þessar einingar voru notaðar til að stofna reiknaðar mælieiningar í gagnalíkani. Þessar reiknaðar mælieiningar eru notaðar til að reikna út afkastavísar (Afkastavísa) og skýrslur sem eru notaðar í innihald þjónustupakka. Ef óskað er að taka með viðbótarútreikning á skýrslur- og mælaborð hægt að sækja og breyta skrá CompensationandBenefits.pbix úr LCS. Þessi skrá er gagnalíkan sjálfgefna sem var notað til að stofna innihald þjónustupakka. Eftir breytingar, hægt er að stofna til fyrirtækis innihald þjónustupakka og mælaborð sem innihalda upplýsingar sem hefur verið bætt við.

## <a name="additional-resources"></a>Frekari upplýsingar
Hér eru gagnlegir tenglar sem tengjast einingar og að búa til Power BI-efni:

-   [Gagnaeiningar](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/)
-   [Stofnun efnispakka fyrirtækis ](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   [Gera gagnalíkön með því að nota Power BI](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [Bæta Power BI-reitum við vinnusvæði](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/07/06/pinning-power-bi-reports-to-dynamics-ax-client/)



