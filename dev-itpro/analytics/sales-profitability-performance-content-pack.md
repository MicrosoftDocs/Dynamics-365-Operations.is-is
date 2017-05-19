---
title: "Sölu- og afköst arðsemisgreiningar Power BI-efni"
description: "Þetta efnisatriði lýsir því sem er innifalið í Dynamics 365 for Operations - Sölu- og arðsemi afköst innihaldi pakka fyrir Microsoft Power BI. Það lýsir einnig hvernig eigi að fara í skýrslur sem eru hafðar með í efnispakkanum, og veitir upplýsingar um gagnalíkan og einingar sem notaðar eru til að búa til efnispakka."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 260674
ms.assetid: ab457f02-929e-4d34-b813-335be3092287
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 35d34f9a356f8a041f2abf0aa8d6c3a6d9ca4a46
ms.contentlocale: is-is
ms.lasthandoff: 04/25/2017


---

# <a name="sales-and-profitability-performance-power-bi-content"></a>Sölu- og afköst arðsemisgreiningar Power BI-efni

[!include[banner](../includes/banner.md)]


Þetta efnisatriði lýsir því sem er innifalið í Dynamics 365 for Operations - Sölu- og arðsemi afköst innihaldi pakka fyrir Microsoft Power BI. Það lýsir einnig hvernig eigi að fara í skýrslur sem eru hafðar með í efnispakkanum, og veitir upplýsingar um gagnalíkan og einingar sem notaðar eru til að búa til efnispakka.

<a name="overview"></a>Yfirlit
--------

Þessi efnispakki var stofnaður fyrir sölustjórnendur til að fylgjast með lykilmælikvörðum sölu yfir tekjur, brúttóhagnað og hagnaður framlegð. Hann notar færslugögn sölu frá Microsoft Dynamics 365 for Operations og veitir bæði samanlagt yfirlit yfir sölutölur fyrirtækisins og sundurliðun söluafkomu fyrir viðskiptavini og afurðir. Með því að merkja breytingar á vexti í tekjum og hagnaði yfir tíma er hægt að nota skýrslur til að vara stjórnendur við jákvæðri og neikvæðri kostnaðarþróun fyrir einstaka lánardrottna og vörur. Tegunda- og svæðisbundnum stjórnendum finnst gagnlegt að bera saman tekjur og arðsemi fyrir ólíkar tegundir afurða og viðskiptavinaflokka til að finna slóða og leiðtoga. Alhliða skýrsla sem dregur upp tekjur á móti hagnaðarhlutfalli staks viðskiptavinar býður lykilstjórnendum gagnaafritaðan grunn að til fínstilla sölu sína og markaðssetningu fyrir viðkomandi forstillingu fyrir hvern viðskiptavin. Efnispakki sölu- og arðsemiafkoma auðveldar sölustjórum að greina söluafkomu eftir:

-   Tekjur, á árinu (með viðskiptavinaflokk og einstaka viðskiptavini, sölutegundir, og stakar afurðir og landsvæði)
-   Tekjubreytingar, ár frá ári (eftir svæði viðskiptavina og söluflokkum)

Hægt er að greina arðsemi eftir:

-   Brúttóhagnaði og hagnaðarframlegð (með því að flokka viðskiptavina og afurðaflokka sölu)
-   Breyting á brúttóframlegð, ár frá ári
-   Arðsemi viðskiptavinar (eftir tekjum á móti brúttóframlegð)

## <a name="accessing-the-content-pack"></a>Farið í efnispakkann
Power BI efnispakki afkomu sölu og arðsemi er gefinn út sem innleiðingareign í Lifecycle Services (LCS) og er hægt að fara í úr Dynamics 365 for Operations. Nánari upplýsingar um hvernig á að fara í og opna Power BI-skýrslur er að finna í [Power BI-efni í LCS frá Microsoft og viðskiptaaðilum þínum](power-bi-content-microsoft-partners.md).
**Athugið:** - KB 4011327 er forskilyrði fyrir þetta Power BI-efni. Eftir að þú skrá inn á Lifecycle Services, hefurðu aðgang að KB hér: <a href="https://fix.lcs.dynamics.com/issue/results/?q=kb4011327">https://fix.lcs.dynamics.com/issue/results/?q=kb4011327</a>.

## <a name="metrics-included-in-the-content-pack"></a>Mælikvarðar sem eru hafðir með í efnispakka
Efnispakkinn inniheldur skýrslu sem samanstendur af safni mælikvarða sem eru sýndir sem myndrit, reitir og töflur. Í eftirfarandi töflu er yfirlit yfir myndbirtingar í efnispakkanum.

|                        |                                            |                                                         |
|------------------------|--------------------------------------------|---------------------------------------------------------|
| **Skýrslusíða**        | **Gröf**                                 | **Reitir**                                               |
| Tekjur eftir viðskiptavini    | Efstu tíu viðskiptamenn eftir tekjum                | Heildartekjur                                           |
|                        | Heildartekjur eftir viðskiptavinaflokki            | Vöxtur í tekjum ár frá ári                                      |
|                        | Heildartekjur viðskiptavina eftir viðskiptavinaflokki | Brúttóframlegð                                            |
|                        | Tekjur & brúttóframlegð eftir viðskiptavinaflokki   |                                                         |
| Tekjur eftir afurðum     | Tekjur & brúttóframlegð eftir söluflokki   | Samtala \# aukaafurða                                    |
|                        | Efstu tíu afurðir eftir tekjum                 | Heildarfjöldi virkra afurða og prósenta af samtölu |
|                        | Heildartekjur eftir söluflokki            | Fjöldi afurða fyrir 80% tekna           |
| Tekjur eftir tímabili\*    | Tekjur eftir mánuði                           | Vöxtur í tekjum ár frá ári                                      |
|                        | Eftirliggjandi tekjufrávik             | Vöxtur í tekjum ár frá ári %                                    |
|                        | Heildarfrávik sölu eftir landsvæði viðskiptavinar    |                                                         |
| Tekjur eftir staðsetningu    | Sölutekjur eftir borg                      |                                                         |
|                        | Vöxtur í tekjum ár frá ári %                       |                                                         |
|                        | Sölutekjur eftir svæðum                    |                                                         |
| Arðsemi viðskiptavinar | Brúttóframlegð á móti tekjum, viðskiptavinum   | Brúttóhagnaður, brúttóframlegð, vöxtur í tekjum ár frá ári          |
| Arðsemisgreining | Tekjur og brúttóhagnaður eftir mánuði          |                                                         |
|                        | Efstu 15 viðskiptamenn eftir brúttóframlegð           |                                                         |
|                        | Brúttóhagnaður eftir mánuði, ár frá ári                 |                                                         |

\* Tekjur þessa árs og síðasta árs og vöxtur eftir söluflokki.

## <a name="understanding-the-data-model-and-entities"></a>Skilja gagnalíkan og einingar
Dynamics 365 for Operations er notað til að fylla út skýrslur í efnispakka Sölu- og arðsemisframmistöðu. Þetta er birt sem uppsafnaðar mælingar sem stigbundnar eru í einingaversluninni sem Microsoft SQL-gagnagrunnur sem er fínstilltur fyrir greiningu. Sjá frekari upplýsingar um það í bloggfærslunni [Power BI samþættingu við einingaverslun í Dynamics](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/). Uppsafnaðar mælingar í þessum efnispakka eru undirflokkur uppsafnaðra mælinga sem voru tiltækar í söluteningi í Dynamics AX 2012 og AX 2012 R3. Til að stilla uppsafnaðar mælingar tenings í einingaverslun, verður að gera þær virkjanlegir. Sjá frekari upplýsingar um ferli fyrir sviðsetningu uppsafnaðra mælinga í einingaverslun í bloggfærslunni [Power BI samþættingu við einingaverslun í Dynamics](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/). Eftirfarandi lykiluppsafnaðar mælingar á reikningslínueiningunni eru notaðar sem grunnur að efnispakka.

|               |                                              |                                                 |                                              |                                          |
|---------------|----------------------------------------------|-------------------------------------------------|----------------------------------------------|------------------------------------------|
| **Eining**    | **Lykiluppsafnaðar mælingar**               | **Gagnaveita fyrir Dynamics 365 for Operations** | **Svæði**                                    | **Lýsing**                          |
| Línur á reikningi | Tekjur                                      | CustInvoiceTrans                                | SAMTALA(LineAmountMST)                           | Upphæð í bókhaldsgjaldmiðli            |
|               | Kostnaður seldra vara                           | InventTrans                                     | SAMTALA(CostAmountPosted + CostAmountAdjustment) | Kostnaðarupphæð + leiðrétting                 |
|               | Línuupphæð þóknunar – bókhaldsgjaldmiðill | CustInvoiceTrans                                | SUM(CommissAmountMST)                        | Upphæð þóknunar í bókhaldsgjaldmiðli |

Eftirfarandi tafla sýnir lykiluppsafnaðar mælingar reikningslínueiningarinnar sem eru notaðar til að stofna nokkrar útreikningsmælingar í efnispakkanum.

|                   |                                                                                                  |
|-------------------|--------------------------------------------------------------------------------------------------|
| **Mælieining**       | **Reiknað sem**                                                                                |
| Brúttóframlegð      | SUM(Tekjur – COGS – Þóknun – Virðisaukaskattur (talinn með í línuupphæð viðskiptavinareiknings))          |
| Brúttóframlegð      | SUM(Brúttóhagnaður/ (Tekjur – Virðisaukaskattur (talinn með í línuupphæð viðskiptavinareiknings)))             |
| Tekjur síðasta árs | Tekjur síðasta árs = REIKNA (SAMTALA ('Reikningslínur'\[Tekjur\]), SAMEPERIODLASTYEAR (Dagsetningar\[Dagsetning\])) |

Eftirfarandi lykilvíddir í **Söluteningi** eru notaðar sem síur til að sneiða uppsafnaðar mælingar þannig að hægt sé að ná meiri uppskiptingu og dýpri greiningarinnsýn.

|                  |                                                      |
|------------------|------------------------------------------------------|
| **Eining**       | **Dæmi um eigindir**                           |
| Viðskiptavinir        | Viðskiptavinaflokkar, Viðskiptavin svæða, Heimilisfang, Atvinnugrein |
| Afurðir         | Afurðarnúmer, afurðarheiti, heiti vöruflokka       |
| Sölutegundir | Heiti söluflokka                                 |
| Lögaðilar   | Heiti lögaðila                                   |
| Dagsetningar            | Dagsetningar                                                |

Sjálfgefið er að efnispakki sýni gögn fyrir núgildandi almanaksár, en hægt er að opna skýrslusíuhlutann og breyta dagsetningarafmörkun. Einnig er hægt að breyta síu fyrirtækisins.

## <a name="additional-resources"></a>Frekari upplýsingar
Hér eru gagnlegir tenglar sem tengjast einingar og að búa til Power BI-efni:

-   [Gagnaeiningar](..\data-entities\data-entities.md)
-   [Stofnun efnispakka fyrirtækis ](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   [Gera gagnalíkön með því að nota Power BI](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [Bæta Power BI-reitum við vinnusvæði](configure-power-bi-integration.md)





