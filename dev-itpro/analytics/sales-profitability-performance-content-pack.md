---
title: "Sölu- og afköst arðsemisgreiningu Power BI-efni"
description: "Þetta efnisatriði lýsir því hvað er innifalin í Dynamics 365 aðgerða - Sölu- og arðsemi afköst innihaldi pakka fyrir Microsoft Power BI. Það útskýrt hvernig á að ná í skýrslur í innihald þjónustupakka og upplýsingar um gagnalíkan og einingar sem notaðar eru til að búa til innihald þjónustupakka."
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
translationtype: Human Translation
ms.sourcegitcommit: 388b6398488e6f316c1ec07a00182e81c1dc8d08
ms.openlocfilehash: 3e6b48768bb8e69d46f1555d9300f3b878b01ff1
ms.lasthandoff: 03/31/2017


---

# <a name="sales-and-profitability-performance-power-bi-content"></a>Sölu- og afköst arðsemisgreiningu Power BI-efni

Þetta efnisatriði lýsir því hvað er innifalin í Dynamics 365 aðgerða - Sölu- og arðsemi afköst innihaldi pakka fyrir Microsoft Power BI. Það útskýrt hvernig á að ná í skýrslur í innihald þjónustupakka og upplýsingar um gagnalíkan og einingar sem notaðar eru til að búa til innihald þjónustupakka.

<a name="overview"></a>Yfirlit
--------

Þessi innihald þjónustupakka var stofnuð fyrir sölustjórnendur til að fylgjast með sölu mælikvörðum lykill yfir tekjur, brúttóhagnað og hagnaður framlegð. Það notar sölu færslugögn úr Dynamics 365 aðgerða og veitir both steypa saman yfirlit fyrirtækið sölu tölur og niðurbrot afköst í sölu fyrir viðskiptavini og vörur. Með því að merkja breytingar í fyrir vöxt tekjur og hagnað tímanum hægt að nota skýrslur stjórnenda viðvörun um leitni jákvætt og neikvætt fyrir einstaka viðskiptavini og vörur. Tegund og svæðisbundið stjórnendur finnur það gagnlegt að bera saman tekjur og arðsemi fyrir tegundum aðra afurð og viðskiptavinaflokka hvor við aðra sem einni út laggards og leaders gröf. Fá alhliða skýrslu sem plots einstökum viðskiptavini tekjur og hagnaðarframlegð tilboð lykil stjórnendur afrita gögn grunn að attune þeirra sölu og markaðssetningar vinna viðkomandi forstillingu fyrir hvern viðskiptavin. Sölu- og arðsemi afköst innihald þjónustupakka gerir stjórnendum Sölu til að greina afköst í sölu eftir:

-   Tekjur, á árinu (með viðskiptavinaflokk og einstaka viðskiptavini, sölutegundir, og stakar afurðir og landsvæði)
-   Breyta tekjur, ár of-ár (eftir svæði og vsk tegundum viðskiptavina)

Hægt er að greina arðsemisgreiningu eftir:

-   Brúttóhagnaður í og hagnaðarframlegð (með því að flokka viðskiptavina og afurðaflokka sölu)
-   Brúttóframlegð breytinguna ár of ár
-   Arðsemi viðskiptavinar (eftir tekjum og brúttóframlegð)

## <a name="accessing-the-content-pack"></a>Fara í hugbúnaðarhlutartréð innihaldi pakka
Sölu- og afköst arðsemisgreiningu Power BI innihald þjónustupakka er birt sem innleiðingu eign í Lifecycle Services (LCS) og hægt er að nálgast Dynamics 365 fyrir Aðgerðir. Nánari upplýsingar um hvernig á að fá aðgang að og ræsa Power BI skýrslur í [Power BI efni í LCS frá Microsoft og for your viðskiptaaðila](power-bi-content-microsoft-partners.md).

## <a name="metrics-included-in-the-content-pack"></a>Í innihald þjónustupakka mælikvörðum
Innihald þjónustupakka inniheldur skýrsla sem samanstendur af safni mælikvörðum visualized sem gröf reitir og töflur. Eftirfarandi tafla veitir yfirlit yfir visualisations í innihald þjónustupakka.

|                        |                                            |                                                         |
|------------------------|--------------------------------------------|---------------------------------------------------------|
| **Skýrslan síðu**        | **Charts**                                 | **Reitir**                                               |
| Tekjur af viðskiptavini    | 10 efstu viðskiptavinir eftir tekjum                | Heildartekjur                                           |
|                        | Heildartekjur eftir viðskiptavinaflokki            | Tekjur vöxt sölu milli ÁRA                                      |
|                        | Tekjur meðaltal viðskiptavina eftir viðskiptavinaflokki | Brúttóframlegð                                            |
|                        | Tekjur & brúttóframlegð eftir viðskiptavini   |                                                         |
| Tekjur eftir afurð     | Tekjur & brúttóframlegð eftir söluflokki   | Samtals \#afurða                                    |
|                        | 10 efstu afurðir eftir tekjum                 | Heildarfjöldi virk afurðir og prósentu af heild |
|                        | Heildartekjur eftir söluflokki            | Fjöldi afurða fyrir 80% tekna           |
| Tekjur eftir tímabili\*    | Tekjur eftir mánuði                           | Tekjur vöxt sölu milli ÁRA                                      |
|                        | Aftast frávik tekjum, sölu milli ÁRA             | % Fyrir vöxt sölu milli ÁRA tekjur                                    |
|                        | Heildarfrávik sölu eftir landsvæði viðskiptavinar    |                                                         |
| Tekjur eftir staðsetningu    | Sölutekjur af borg                      |                                                         |
|                        | % Fyrir vöxt sölu milli ÁRA tekjur                       |                                                         |
|                        | Sölutekjur af svæði                    |                                                         |
| Skýrsla um arðsemisgreiningu viðskiptavinar | Brúttóframlegð eða tekjur eftir viðskiptavini   | Brúttóframlegð, brúttóframlegð, vöxt sölu milli ÁRA tekjur          |
| Arðsemisgreining | Tekjur og brúttóframlegð eftir mánuði          |                                                         |
|                        | 15 efstu viðskiptavinir eftir brúttóframlegð           |                                                         |
|                        | Brúttóframlegð eftir mánuði, sölu milli ÁRA                 |                                                         |

\*Tekjur þetta og síðasta ári, og vöxt eftir söluflokki.

## <a name="understanding-the-data-model-and-entities"></a>Skilja gagnalíkan og einingar
Dynamics 365 fyrir Aðgerðir er notuð til að fylla skýrsluna í Sölu- og arðsemi afköst innihald þjónustupakka. Þetta er birtur sem uppsöfnuðum mælingum sem stig eru í versluninni Einingar sem er bestuð fyrir greiningu gagnagrunni Microsoft SQL. Lesa meira um það á við blog [Power BI samþættingu við Verslunina Einingar í Dynamics](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/). Uppsafnaðar mælingar í þessa innihald þjónustupakka eru undirsetti uppsöfnuðum mælingum sem voru tiltæk í Sölutening í Dynamics AX 2012 og AX 2012 R3. Áfangi uppsafnaðar mælingar tenings í versluninni Einingar sem verður að gera þær virkjanlegir. Nánari upplýsingar, sjá ferli um áfangi uppsafnaðar mælingar í verslun Einingar í á blog [Power BI samþættingu við Verslunina Einingar í Dynamics](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/). Í eftirfarandi lykill uppsöfnuðum mælingum einingarinnar Reiknings línur eru notaðar sem grunnur innihald þjónustupakka.

|               |                                              |                                                 |                                              |                                          |
|---------------|----------------------------------------------|-------------------------------------------------|----------------------------------------------|------------------------------------------|
| **Entity**    | **Uppsafnaðar mælingar lykli**               | **Gagnagjafi fyrir Dynamics 365 fyrir Aðgerðir** | **Field**                                    | **Description**                          |
| Línur á reikningi | Tekjur                                      | CustInvoiceTrans                                | SUM(LineAmountMST)                           | Upphæð í bókhaldsgjaldmiðli            |
|               | Kostnaður seldra vara                           | InventTrans                                     | SAMTALA (CostAmountPosted + CostAmountAdjustment) | Kostnaðarupphæð + leiðrétting                 |
|               | Línuupphæð þóknunar-bókhaldsgjaldmiðill | CustInvoiceTrans                                | SUM(CommissAmountMST)                        | Upphæð þóknunar í bókhaldsgjaldmiðli |

Eftirfarandi tafla sýnir sem lykill uppsöfnuðum mælingum einingarinnar reiknings línur sem eru notaðar til að stofna reiknaðar mælieiningar í innihaldi pakka dataset.

|                   |                                                                                                  |
|-------------------|--------------------------------------------------------------------------------------------------|
| **Measure**       | **Reiknuð sem**                                                                                |
| Brúttóframlegð      | SAMTALA (Tekjur – kostnaður seldra VARA-Þóknun – virðisaukaskatt (með í línuupphæð viðskiptavinareiknings))          |
| Brúttóframlegð      | SAMTALA (Brúttóframlegðar / (Veltu - virðisaukaskattur (innifalinn í línuupphæð viðskiptavinareiknings)))             |
| Tekjur síðasta árs | Tekjur síðasta árs = REIKNA (SAMTALA ('Reikningslínur'\[Tekjur\]), SAMEPERIODLASTYEAR (Dagsetningar\[Dagsetning\]) |

Eftirfarandi lykill víddir í á **sölutening** eru notuð sem síur til að sneiða uppsöfnuðum mælingum sem á að ná hærri uppskiptingin og hærra insights greiningar.

|                  |                                                      |
|------------------|------------------------------------------------------|
| **Entity**       | **Dæmi um eigindir**                           |
| Viðskiptavinir        | Viðskiptavinaflokkar, Viðskiptavin svæða, Heimilisfang, Atvinnugrein |
| Afurðir         | Afurðarnúmer, afurðarheiti, vöruheiti flokka       |
| Sölutegundir | Heiti söluflokk                                 |
| Lögaðilar   | Heiti lögaðila                                   |
| Dagsetningar            | Dagsetningar                                                |

Að sjálfgefnu innihald þjónustupakka birtir gögn fyrir núgildandi almanaksár, en hægt er að opna hlutann síur skýrslu og breyta dagsetningu síu. Einnig er hægt að breyta síu fyrirtækisins.

## <a name="additional-resources"></a>Frekari upplýsingar
Hér eru gagnlegir tenglar sem tengjast einingar og að búa til Power BI-efni:

-   [Gagnaeiningar](..\data-entities\data-entities.md)
-   [Stofnun efnispakka fyrirtækis ](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   [Gera gagnalíkön með því að nota Power BI](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [Bæta Power BI-reitum við vinnusvæði](configure-power-bi-integration.md)



