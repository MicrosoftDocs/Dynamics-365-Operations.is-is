---
title: "Framleiðsluafköst - Power BI efni"
description: "Þetta efnisatriði lýsir því hvað felst í Power BI efninu Framleiðsluafköst. Það lýsir einnig hvernig eigi að fara í Power BI-skýrslur og veitir upplýsingar um gagnalíkan og einingar sem notaðar voru til að búa til efnið."
author: AndersGirke
manager: AnnBe
ms.date: 12/19/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: ProductionPerformancePowerBI
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 821d8927211d7ac3e479848c7e7bef9f650d4340
ms.openlocfilehash: 2bc4c409b831b78ef737a98ce985bf144853a454
ms.contentlocale: is-is
ms.lasthandoff: 08/13/2018

---

# <a name="production-performance-power-bi-content"></a>Framleiðsluafköst - Power BI efni

[!include [banner](../includes/banner.md)]

Þetta efnisatriði lýsir því hvað er innifalið í Microsoft Power BI efninu **Framleiðsluafköst**. Það lýsir einnig hvernig eigi að fara í Power BI-skýrslur og veitir upplýsingar um gagnalíkan og einingar sem notaðar voru til að búa til efnið.

## <a name="overview"></a>Yfirlit

Power BI efnið **Framleiðsluafköst** er fyrir framleiðslustjóra eða einstaklinga í fyrirtækinu sem bera ábyrgð á framleiðslustýringu.

Skýrslur sem eru innifaldar gera þér kleift að nota Power BI til að fylgjast með afköstum framleiðsluaðgerða með hliðsjón af tímanlegri framkvæmd, gæðum og kostnaði. Skýrslurnar nota færslugögn úr framleiðslupöntunum og runupöntunum og gefa bæði samantekna sýn yfir framleiðslumælieiningar yfir allt fyrirtækið og sundurliðun á mælieiningum eftir afurðum og tilföngum.

Í Power BI efninu er lögð áhersla á getu fyrirtækisins til að ljúka við framleiðslu á réttum tíma og til fulls. Spáð er um framtíðarafköst á grundvelli framleiðsluáætlana. Ítarlegar skýrslur veita gott innsæi í framleiðslugalla sem orsakast af framleiðslu og einnig tíðni galla í tilföngum og aðgerðum.

Með þessu Power BI efni er einnig hægt að greina framleiðslufrávik. Framleiðslufrávik eru reiknuð sem mismunurinn milli áætlaðs kostnaðar og raunkostnaðar. Frávik í framleiðslu eru reiknuð þegar framleiðslupantanir eða runupantanir ná stöðunni **Lokið**.

Power BI efnið **Framleiðsluafköst** hefur að geyma gögn sem eiga uppruna sinn í framleiðslupöntunum og runupöntunum. Skýrslurnar innihalda ekki gögn sem tengjast kanban-framleiðslu.

## <a name="accessing-the-power-bi-content"></a>Farið í Power BI-efni
**Framleiðsluafköst** Power BI efni er sýnt á **Framleiðsluafköst** síðunni (**Framleiðslustýring** \> **Fyrirspurnir og skýrslur** \> **Greining á framleiðsluafköstum** \> **Framleiðsluafköst**). 

## <a name="metrics-that-are-included-in-the-power-bi-content"></a>Mælikvarðar sem eru hafðir með í Power BI-efni

Power BI efnið **Framleiðsluafköst** felur í sér safn af skýrslusíðum. Hver síða samanstendur af safni mælikvarða sem eru sýndir sem myndrit, reitir og töflur.

Eftirfarandi tafla sýnir myndræna framsetningu sem fylgir.

| Skýrslusíða                                | Gröf | Reitir |
|--------------------------------------------|--------|-------|
| Framleiðsluafköst                     | <ul><li>Framleiðslufjöldi eftir dagsetningu</li><li>Framleiðslugjöld eftir afurð og vöruhóp</li><li>Fjöldi áætlaðrar framleiðslu eftir dagsetningu</li><li>Neðstu 10 afurðir eftir tíma &amp; tæmandi</li></ul> | <ul><li>Heildarpantanir</li><li>Á tíma &amp; tæmandi %</li><li>Ólokið %</li><li>Á undan áætlun %</li><li>Á eftir áætlun %</li></ul> |
| Gallar eftir afurð                         | <ul><li>Hlutfall galla (milljónarhluti) eftir dagsetningu</li><li>Hlutfall galla (milljónarhluti) eftir afurð og vöruhóp</li><li>Framleitt magn eftir dagsetningu</li><li>Efstu 10 vörur eftir skilvirknitíðni</li></ul> | <ul><li>Hlutfall galla (milljónarhluti)</li><li>Magn gallaðs</li><li>Heildarmagn</li></ul> |
| Gallaþróun eftir afurð                   | Hlutfall galla (milljónarhluti) eftir framleiddu magni | Hlutfall galla (milljónarhluti) |
| Gallar eftir tilföngum                        | <ul><li>Hlutfall galla (milljónarhluti) eftir dagsetningu</li><li>Hlutfall galla (milljónarhluti) eftir tilföngum og svæði</li><li>Hlutfall galla (milljónarhluti) eftir aðgerð</li><li>Efstu 10 tilföng eftir hlutfalli galla</li></ul> | Magn gallaðs |
| Gallaþróun eftir tilföngum                  | Hlutfall galla (milljónarhluti) eftir unnu magni | |
| Framleiðslufrávik fyrir kostnaðaraðferð vinnslupöntunar | <ul><li>Framleiðslufrávik eftir dagsetningu og gerð kostnaðarflokks</li><li>Framleiðslufrávik eftir svæði og gerð kostnaðarflokks</li><li>Efstu 10 vörur með óhagstætt framleiðslufrávik</li><li>Efstu 10 vörur með óhagstætt framleiðslufrávik eftir tilföngum</li></ul> | <ul><li>Innleystur kostnaður</li><li>Framleiðslufrávik</li><li>Framleiðslufrávik %</li></ul> |


## <a name="understanding-the-data-model-and-entities"></a>Skilja gagnalíkan og einingar

Eftirfarandi gögn eru notuð fyrir skýrslusíðurnar í Power BI efninu **Framleiðsluafköst**. Þessi gögn eru birt sem uppsafnaðar mælingar sem stigbundnar eru í einingaversluninni. Entity-verslunin er Microsoft SQL-gagnagrunnur sem er fínstilltur fyrir greiningu. Frekari upplýsingar um einingaverslunina má fá í [samþættingu Power BI við einingaverslunina](power-bi-integration-entity-store.md).

Eftirfarandi tafla sýnir helstu uppsöfnuðu mælingarnar sem eru notaðar sem grundvöllur fyrir Power BI efnið

| Eining                   | Lykiluppsafnaðar mælingar  | Gagnagjafi fyrir Finance and Operations | Svæði              |
|--------------------------|-----------------------------|----------------------------------------|--------------------|
| CostCalculation          | CostAmount                  | ProdCalcTransExpanded                  | CostAmount         |
| CostCalculation          | CostMarkup                  | ProdCalcTransExpanded                  | CostMarkup         |
| CostCalculation          | ActualCostAmount            | ProdCalcTransExpanded                  | RealCostAmount     |
| CostCalculation          | RealCostAdjustment          | ProdCalcTransExpanded                  | RealCostAdjustment |
| RouteTransactions        | ErrorQuantity               | ProdRouteTransExpanded                 | QtyError           |
| RouteTransactions        | GoodQuantity                | ProdRouteTransExpanded                 | QtyGood            |
| ProductionOrder          | DaysDelayed                 | ProdTableExpanded                      | DaysDelayed        |
| ProductionOrder          | LeadTime                    | ProdTableExpanded                      | LeadTime           |
| ProductionOrder          | PlannedLeadTime             | ProdTableExpanded                      | PlannedLeadTime    |
| ProductionOrder          | ProductionOrderCount        | ProdTableExpanded                      |                    |
| CoproductCostCalculation | CoproductCostAmount         | PmfCoByProdCalcTransExpanded           | CostAmount         |
| CoproductCostCalculation | CoproductCostMarkup         | PmfCoByProdCalcTransExpanded           | CostMarkup         |
| CoproductCostCalculation | CoproductRealCostAdjustment | PmfCoByProdCalcTransExpanded           | RealCostAdjustment |
| CoproductCostCalculation | CoproductActualCostAmount   | PmfCoByProdCalcTransExpanded           | RealCostAmount     |

Eftirfarandi tafla sýnir hvernig lykiluppsafnaðar mælingar eru notaðar til að stofna nokkrar útreikningsmælingar í gagnamengi efnisins.

| Mæla                  | Hvernig mælieining er reiknuð |
|--------------------------|-------------------------------|
| Framleiðslufrávik, %   | SUM(„Framleiðslufrávik“\[„Framleiðslufrávik“\]) / SUM(„Framleiðslufrávik“\[Áætlaður kostnaður\]) |
| Allar áætlaðar pantanir       | COUNTROWS('Áætlaðar framleiðslupantanir') |
| Á undan áætlun                    | COUNTROWS(FILTER („Áætluð framleiðslupöntun“, „Áætluð framleiðslupöntun“\[Áætluð lokadagsetning\] \< „Áætluð framleiðslupöntun“\[Dagsetning þarfa\])) |
| Á eftir áætlun                     | COUNTROWS(FILTER(„Áætluð framleiðslupöntun“, „Áætluð framleiðslupöntun“\[Áætluð lokadagsetning\] \> „Áætluð framleiðslupöntun“\[Dagsetning þarfa\])) |
| Á réttum tíma                  | COUNTROWS(FILTER(„Áætluð framleiðslupöntun“, „Áætluð framleiðslupöntun“\[Áætluð lokadagsetning\] = „Áætluð framleiðslupöntun“\[Dagsetning þarfa\])) |
| Á réttum tíma %                | IF („Áætluð framleiðslupöntun“\[Á réttum tíma\] \<\> 0, „Áætluð framleiðslupöntun“\[Á réttum tíma\], IF („Áætluð framleiðslupöntun“\[Allar áætlaðar pantanir\] \<\> 0, 0, BLANK()) ) / „Áætluð framleiðslupöntun“\[Allar áætlaðar pantanir\] |
| Lok.                | COUNTROWS(FILTER(„Framleiðslupöntun“, „Framleiðslupöntun“\[Er með RAF\] = TRUE)) |
| Hlutfall galla (milljónarhluti)     | IF („Framleiðslupöntun“\[Heildarmagn\] = 0, BLANK(), (SUM(„Framleiðslupöntun“\[Gallað magn\]) / „Framleiðslupöntun“\[Heildarmagn\]) \* 1000000) |
| Tíðni framleiðslustafa  | „Framleiðslupöntun“\[Á eftir áætlun \#\] / „Framleiðslupöntun“\[Lokið\] |
| Á réttum tíma og tæmandi          | COUNTROWS(FILTER(„Framleiðslupöntun“, „Framleiðslupöntun“\[Er tæmandi\] = TRUE && „Framleiðslupöntun“\[Er á undan áætlun\] = TRUE)) |
| Á undan áætlun \#                 | COUNTROWS(FILTER(„Framleiðslupöntun“, „Framleiðslupöntun“\[Er á undan áætlun\] = TRUE)) |
| Á undan áætlun %                  | IFERROR( IF(„Framleiðslupöntun“\[Á undan áætlun \#\] \<\> 0, „Framleiðslupöntun“\[Á undan áætlun \#\], IF(„Framleiðslupöntun“\[Heildarpantanir\] = 0, BLANK(), 0)) / „Framleiðslupöntun“\[Heildarpantanir\], BLANK()) |
| Ófullgert               | COUNTROWS(FILTER(„Framleiðslupöntun“, „Framleiðslupöntun“\[Er tæmandi\] = FALSE && „Framleiðslupöntun“\[Er með RAF\] = TRUE)) |
| Ólokið %             | IFERROR( IF(„Framleiðslupöntun“\[Ólokið\] \<\> 0, „Framleiðslupöntun“\[Ólokið\], IF(„Framleiðslupöntun“\[Heildarpantanir\] = 0, BLANK(), 0)) / „Framleiðslupöntun“\[Heildarpantanir\], BLANK()) |
| Seinkar               | „Framleiðslupöntun“\[Er með RAF\] = TRUE && „Framleiðslupöntun“\[Seinkað gildi\] = 1 |
| Er á undan áætlun                 | „Framleiðslupöntun“\[Er með RAF\] = TRUE && „Framleiðslupöntun“\[Seinkun í dögum\] \< = 0 |
| Er tæmandi               | „Framleiðslupöntun“\[Gott magn\] \>= „Framleiðslupöntun“\[Áætlað magn\] |
| Er með RAF                | „Framleiðslupöntun“\[Framleiðslustöðugildi\] = 5 \|\| „Framleiðslupöntun“\[Framleiðslustöðugildi\] = 7 |
| Á eftir áætlun og tæmandi           | COUNTROWS(FILTER(„Framleiðslupöntun“, „Framleiðslupöntun“\[Er tæmandi\] = TRUE && „Framleiðslupöntun“\[Seinkar\] = TRUE)) |
| Á eftir áætlun \#                  | COUNTROWS(FILTER(„Framleiðslupöntun“, „Framleiðslupöntun“\[Seinkar\] = TRUE)) |
| Á eftir áætlun %                   | IFERROR( IF(„Framleiðslupöntun“\[Seinkun \#\] \<\> 0, „Framleiðslupöntun“\[Seinkun \#\], IF(„Framleiðslupöntun“\[Heildarpantanir\] = 0, BLANK(), 0)) / „Framleiðslupöntun“\[Heildarpantanir\], BLANK()) |
| Á réttum tíma og tæmandi        | COUNTROWS(FILTER(„Framleiðslupöntun“, „Framleiðslupöntun“\[Er tæmandi\] = TRUE && „Framleiðslupöntun“\[Seinkar\] = FALSE && „Framleiðslupöntun“\[Er á undan áætlun\] = FALSE)) |
| Á réttum tíma og tæmandi %      | IFERROR( IF(„Framleiðslupöntun“\[Á réttum tíma og tæmandi\] \<\> 0, „Framleiðslupöntun“\[Á réttum tíma og tæmandi\], IF(„Framleiðslupöntun“\[Lokið\] = 0, BLANK(), 0)) / „Framleiðslupöntun“\[Lokið\], BLANK()) |
| Heildarpantanir             | COUNTROWS('Framleiðslupöntun') |
| Heildarmagn           | SUM („Framleiðslupöntun“\[Gott magn\]) + SUM(„Framleiðslupöntun“\[Gallað magn\]) |
| Hlutfall galla (milljónarhluti)        | IF( „Leiðarfærslur“\[Unnið magn\] = 0, BLANK(), (SUM(„Leiðarfærslur“\[Gallað magn\]) / „Leiðarfærslur“\[Unnið magn\]) \* 1000000) |
| Blandað hlutfall galla (milljónarhluti) | IF( „Leiðarfærslur“\[Samtals blandað magn\] = 0, BLANK(), (SUM(„Leiðarfærslur“\[Gallað magn\]) / „Leiðarfærslur“\[Samtals blandað magn\]) \* 1000000) |
| Unnið magn       | SUM(„Leiðarfærslur“\[Gott magn\]) + SUM(„Leiðarfærslur“\[Gallað magn\]) |
| Samtals blandað magn     | SUM(„Framleiðslupöntun“\[Gott magn\]) + SUM(„Leiðarfærslur“\[Gallað magn\]) |

Eftirfarandi tafla sýnir lykilvíddir sem eru notaðar sem síur til að sneiða uppsafnaðar mælingar þannig að hægt sé að ná meiri uppskiptingu og öðlast betri innsýn í greiningu.

| Eining                    | Dæmi um eigindir                                        |
|---------------------------|---------------------------------------------------------------|
| Skráður lokadagur | Lokadagsetning (RAF), mánuður og upphafsár                 |
| Lokið þann                | Upphaf lokamánaðar og mánuður                                  |
| Dagsetning þarfa          | Upphafsmánuður þarfadagsetningar og þarfadagsetning            |
| Leiðarfærsludagsetning    | Upphafsmánuður leiðarfærslu og dagsetning                       |
| Svæði                     | Auðkenni svæðis, nafn svæðis, ríki og borg                          |
| Einingar                  | Auðkenni og heiti                                                   |
| Tilföng                 | Auðkenni tilfanga, heiti tilfanga, gerð tilfanga og tilfangahópur |
| Afurðir                  | Afurðarnúmer, afurðarheiti, auðkenni vöru og vöruflokkur         |

