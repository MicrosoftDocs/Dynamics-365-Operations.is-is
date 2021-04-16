---
title: Kostnaðarstjórnun Power BI efni
description: Þetta efnisatriði lýsir því hvað er innifalið í kostnaðarstjórnun Power BI efnis.
author: ShylaThompson
ms.date: 03/16/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CostAdminWorkspace, CostAnalysisWorkspace, CostObjectWithLowestAccuracy, CostVarianceChart, CostObjectWithLowestTurn
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 270314
ms.assetid: 9680d977-43c8-47a7-966d-2280ba21402a
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kfend
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fc033e41d17c8bb4c187db60faeefab453b6057a
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5755477"
---
# <a name="cost-management-power-bi-content"></a>Kostnaðarstjórnun Power BI efni

[!include [banner](../includes/banner.md)]

## <a name="overview"></a>Yfirlit

**Kostnaðarstjórnun**  Microsoft Power BI er ætlað fyrir bókhaldara birgða eða einstaklinga innan fyrirtækisins sem bera ábyrgð á hafa áhuga á birgðastöðu eða verki í vinnslu (VÍV), eða sem bera ábyrgð á eða hafa áhuga á að greina frávik staðalkostnaðar.

> [!NOTE]
> **Kostnaðarstjórnun** Power BI efnið sem lýst er hér í þessu efnisatriði gildir um Dynamics 365 Finance and Operations 8.0.
> 
> **Kostnaðarstjórnun** Power BI efnispakki, tiltækur á AppSource síðuna, hefur verið felldur úr gildi. Frekari upplýsingar um þá úreldingu er að finna í [Fjarlægðir eða úreltir eiginleikar fyrir Finance and Operations](../migration-upgrade/deprecated-features.md#power-bi-content-packs-available-on-appsource).

Þetta Power BI efni útvegar flokkað snið sem hjálpar þér að fylgjast með afköstum birgða og sjá hvernig kostnaðurinn rennur í gegnum þær. Hægt er að öðlast innsýn í reksturinn, t.d. veltuhlutfall, fjöldi daga sem birgðir á lager, nákvæmni og „ABC-flokkun“ á völdu samanlögðu stigi (fyrirtæki, vöru, vöruflokki eða stað). Upplýsingarnar sem boðið er upp á er einnig hægt að nota sem ítarlega viðbót við fjárhagsskýrslu.

Power BI-efnið er byggt á samanlagðri mælingu **CostObjectStatementCacheMonthly** sem hefur töfluna **CostObjectStatementCache** sem aðalgagnagjafa. Þessari töflu er stjórnað af ramma skyndiminnis gagnasafns. Sjálfgefið er að taflan sé uppfærð á 24 tíma fresti en hægt er að breyta uppfærslutíðninni eða virkja handvirkar uppfærslur í grunnstillingu gagnasafns skyndiminnis. Hægt er að keyra handvirkar uppfærslur í annaðhvort vinnusvæðinu **Kostnaðarstjórnun** eða vinnusvæðinu **Kostnaðargreining**.

Eftir hverja uppfærslu á töflunni **CostObjectStatementCache** verður að uppfæra samanlagðar mælingar **CostObjectStatementCacheMonthly** áður en gögn í myndrænni framsetningu Power BI eru uppfærð.

## <a name="accessing-the-power-bi-content"></a>Aðgangur að Power BI efni

**Kostnaðarstjórnun** Power BI efnið er sýnt í vinnusvæðunum **Kostnaðarstjórnun** og **Kostnaðargreining**.

Vinnusvæðið **Kostnaðarstjórnun** inniheldur eftirfarandi flipa:

- **Yfirlit** – Þessi flipi sýnir forritsgögn.
- **Staða birgðabókhalds** – Þessi flipi sýnir Power BI-efni.
- **Staða framleiðslubókahalds** – Þessi flipi sýnir Power BI-efni.

Vinnusvæðið **Kostnaðargreining** inniheldur eftirfarandi flipa:

- **Yfirlit** – Þessi flipi sýnir forritsgögn.
- **Greining birgðabókhalds** – Þessi flipi sýnir Power BI-efni.
- **Greining framleiðslubókhalds** – Þessi flipi sýnir Power BI-efni.
- **Greining staðalkostnaðarfráviks** – Þessi flipi sýnir Power BI-efni.

## <a name="report-pages-that-are-included-in-the-power-bi-content"></a>Tilkynna síður sem eru innifaldar í Power BI-efninu

**Kostnaðarstjórnun** Power BI efnið inniheldur safn af skýrslusíðum sem samanstanda af safni mælikvarða. Þessir mælikvarðar eru birtir sem myndrit, reitir og töflur. 

Í eftirfarandi töflum eru yfirlit yfir myndbirtingar í **Kostnaðarstjórnun** Power BI efninu.

### <a name="inventory-accounting-status"></a>Staða birgðabókhalds

| Skýrslusíða                               | Myndbirting                                   |
|-------------------------------------------|-------------------------------------------------|
| Yfirlit yfir birgðir                        | Upphafsstaða                               |
|                                           | Nettó breyting                                      |
|                                           | Nettóbreyting %                                    |
|                                           | Lokastaða                                  |
|                                           | Birgðanákvæmni                              |
|                                           | Veltuhraði birgða                        |
|                                           | Dagar lagerbirgða                          |
|                                           | Virk afurð á tímabili                        |
|                                           | Virkir kostnaðarhlutir á tímabili                   |
|                                           | Staða eftir vöruflokki                           |
|                                           | Staða eftir svæði                                 |
|                                           | Yfirlit eftir flokki                           |
|                                           | Nettóbreyting eftir fjórðungi                           |
| Birgðayfirlit eftir svæði og vöruflokki | Birgðanákvæmni eftir svæði                      |
|                                           | Hlutfall birgðaveltu eftir svæði                |
|                                           | Lokastaða birgða eftir svæði                |
|                                           | Birgðanákvæmni eftir vöruflokki                |
|                                           | Hlutfall birgðaveltu eftir vöruflokki          |
|                                           | Lokastaða birgða eftir svæði og vöruflokki |
| Birgðayfirlit                       | Birgðayfirlit                             |
| Birgðayfirlit eftir svæði               | Birgðayfirlit eftir svæði                     |
| Birgðayfirlit eftir afurðastigveldi  | Birgðayfirlit                             |
| Birgðayfirlit eftir afurðastigveldi  | Birgðayfirlit eftir svæði                     |

### <a name="manufacturing-accounting-status"></a>Staða bókhalds framleiðslu

| Skýrslusíða                | Myndbirting                       |
|----------------------------|-------------------------------------|
| VÍV yfirlit á árinu           | Upphafsstaða                   |
|                            | Nettó breyting                          |
|                            | Nettóbreyting %                        |
|                            | Lokastaða                      |
|                            | VÍV-veltuhlutfall                  |
|                            | Dagar VÍV á lager                    |
|                            | Virkur kostnaðarhlutur á tímabili        |
|                            | Nettóbreyting eftir tilfangaflokki        |
|                            | Staða eftir svæði                     |
|                            | Yfirlit eftir flokki               |
|                            | Nettóbreyting eftir fjórðungi               |
| VÍV-yfirlit              | Upphafsstaða                   |
|                            | Lokastaða                      |
|                            | VÍV-yfirlit eftir flokki           |
| VÍV-yfirlit eftir svæði      | Upphafsstaða                   |
|                            | Lokastaða                      |
|                            | VÍV-yfirlit eftir flokki og svæði  |
| VÍV-yfirlit eftir stigveldi | Upphafsstaða                   |
|                            | Lokastaða                      |
|                            | VÍV-yfirlit eftir flokkastigveldi |

### <a name="inventory-accounting-analysis"></a>Birgðabókhaldsgreining

| Skýrslusíða        | Myndbirting                                                                |
|--------------------|------------------------------------------------------------------------------|
| Upplýsingar um birgðir  | Topp 10 tilföng eftir lokastöðu                                           |
|                    | Topp 10 tilföng eftir aukningu á nettóbreytingu                                      |
|                    | Topp 10 tilföng eftir minnkun á nettóbreytingu                                      |
|                    | Topp 10 tilföng eftir hlutfalli birgðaveltu                                 |
|                    | Tilföng eftir hlutfalli lágrar birgðaveltu og lokastöðu yfir þröskuldi |
|                    | Topp 10 tilföng eftir lítilli nákvæmni                                             |
| ABC-flokkun | Lokastaða birgða                                                     |
|                    | Notað efni                                                            |
|                    | Selt (kostnaður seldra vara)                                                                  |
| Birgðaframvinda   | Lokastaða birgða                                                     |
|                    | Nettóbreyting birgða                                                         |
|                    | Veltuhraði birgða                                                     |
|                    | Birgðanákvæmni                                                           |

### <a name="manufacturing-accounting-analysis"></a>Greining bókhalds framleiðslu

| Skýrslusíða | Myndbirting      |
|-------------|--------------------|
| VÍV-framvinda  | Lokastaða VÍV |
|             | Nettóbreyting VÍV     |
|             | VÍV-veltuhlutfall |

### <a name="std-cost-variance-analysis"></a>Greining á stöðluðum kostnaðarfrávikum

| Skýrslusíða                             | Myndbirting                                        |
|-----------------------------------------|------------------------------------------------------|
| Frávik innkaupsverðs (staðlaður kostnaður) á árinu | Innkaupastaða                                     |
|                                         | Frávik innkaupsverða                              |
|                                         | Hlutfall fráviks innkaupsverða                        |
|                                         | Frávik eftir vöruflokki                               |
|                                         | Frávik eftir svæði                                     |
|                                         | Innkaupsverð eftir fjórðungi                            |
|                                         | Innkaupsverð eftir fjórðungi og vöruflokki             |
|                                         | Topp 10 tilföng eftir hlutfalli óhagstæðra innkaupsverða |
|                                         | Topp 10 tilföng eftir hlutfalli hagstæðra innkaupsverða   |
| Framleiðslufrávik (staðlaður kostnaður) á árinu     | Kostnaður við framleiðslu                                    |
|                                         | Framleiðslufrávik                                  |
|                                         | Hlutfall framleiðslufráviks                            |
|                                         | Frávik eftir vöruflokki                               |
|                                         | Frávik eftir svæði                                     |
|                                         | Framleiðslufrávik eftir fjórðungi                       |
|                                         | Framleiðslufrávik eftir fjórðungi og tegund fráviks     |
|                                         | Topp 10 tilföng eftir óhagstæðum framleiðslufrávikum  |
|                                         | Topp 10 tilföng eftir hagstæðum framleiðslufrávikum    |

## <a name="understanding-the-data-model-and-entities"></a>Skilja gagnalíkan og einingar

Gögn úr forritinu eru notuð til að fylla skýrslusíðurnar í **Kostnaðarstjórnun** Power BI-efni. Þessi gögn eru birt sem uppsafnaðar mælingar sem stigbundnar eru í einingaversluninni sem er Microsoft SQL Server gagnagrunnur sem er fínstilltur fyrir greiningu. Nánari upplýsingar er að finna í [Power BI samþætting við einingaverslun](power-bi-integration-entity-store.md).

Lykiluppsafnaðar mælingar á eftirfarandi hlutum eru notaðar sem grundvöllur Power BI-efnis.

| Hlutur                          | Lykiluppsafnaðar mælingar | Slóð gagnagjafa fyrir Finance and Operations | Svæði               |
|---------------------------------|----------------------------|----------------------------------------|---------------------|
| CostObjectStatementCacheMonthly | Upphæð                     | CostObjectStatementCache               | Upphæð              |
| CostObjectStatementCacheMonthly | Magn                   | CostObjectStatementCache               | Magn                 |
| CostInventoryAccountingKPIGoal  | AnnualInventoryTurn        | CostInventoryAccountingKPIGoal         | AnnualInventoryTurn |
| CostInventoryAccountingKPIGoal  | InventoryAccuracy          | CostInventoryAccountingKPIGoal         | InventoryAccuracy   |

Eftirfarandi tafla sýnir helstu útreiknuðu mælingarnar í Power BI-efninu.

| Ráðstöfun                            | Útreikningur |
|------------------------------------|-------------|
| Upphafsstaða                  | Upphafsstaða = \[Lokastaða\]-\[Nettóbreyting\] |
| Upphafsstaða magns             | Upphafsstaða magns = \[Lokastaða magns\]-\[Nettóbreytingar magns\] |
| Lokastaða                     | Lokastaða = (CALCULATE(SUM(\[Upphæð\]), FILTER(ALL(FiscalCalendar), FiscalCalendar\[MONTHSTARTDATE\] \<= MAX(FiscalCalendar\[MONTHSTARTDATE\])))) |
| Lokastaða magns                | Lokastaða magns = CALCULATE(SUM(\[QTY\]), FILTER(ALL(FiscalCalendar), FiscalCalendar\[MONTHSTARTDATE\] \<= MAX(FiscalCalendar\[MONTHSTARTDATE\]))) |
| Nettó breyting                         | Nettóbreyting = SUM(\[AMOUNT\]) |
| Nettóbreyting magns                    | Nettóbreyting magns = SUM(\[QTY\]) |
| Hlutfall birgðaveltu eftir upphæð | Hlutfall birgðaveltu eftir upphæð = if(OR(\[Meðaltalsstaða birgða\] \<= 0, \[Inventory sold or consumed issues\] \>= 0), 0, ABS(\[Atriði er varðar seldar eða notaðar birgðir\])/\[Meðaltalsstaða birgða\]) |
| Meðaltalsstaða birgða          | Meðaltalsstaða birgða = ((\[Lokastaða\] + \[Upphafsstaða\]) / 2) |
| Dagar lagerbirgða             | Dagar lagerbirgða = 365 / CostObjectStatementEntries\[Hlutfall birgðaveltu eftir upphæð\] |
| Birgðanákvæmni                 | Birgðanákvæmni eftir upphæð = IF(\[Lokastaða\] \<= 0, IF(OR(\[Inventory counted amount\] \<\> 0, \[Lokastaða\] \< 0), 0, 1), MAX(0, (\[Lokastaða\] - ABS(\[Talin upphæð birgða\]))/\[Lokastaða\])) |

Eftirfarandi lykilvíddir eru notaðar sem síur til að sneiða uppsafnaðar mælingar þannig að hægt sé að veita meiri uppskiptingu og dýpri greiningarinnsýn.


| Eining                                                  | Dæmi um eigindir                          |
|---------------------------------------------------------|-------------------------------------------------|
| Afurðir                                                | Afurðarnúmer, afurðarheiti, eining, vöruflokkar |
| Flokkastigveldi (úthlutað á hlutverki Kostnaðarstjórnunar) | Flokkastigveldi, flokkastig              |
| Lögaðilar                                          | Heiti lögaðila                              |
| Fjárhagsdagatöl                                        | Fjárhagsdagatal, ár, ársfjórðungur, tímabil, mánuður   |
| Svæði                                                    | Kenni, nafn, heimilisfang, ríki, land               |


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]