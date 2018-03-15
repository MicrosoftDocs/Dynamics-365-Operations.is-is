---
title: "Kostnaðarstjórnun Power BI efni"
description: "Þetta efnisatriði lýsir því hvað er innifalið í Power BI-efni kostnaðarstjórnunar."
author: YuyuScheller
manager: AnnBe
ms.date: 02/02/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.custom: 270314
ms.assetid: 9680d977-43c8-47a7-966d-2280ba21402a
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7b5c4428c8610a7b2d4cf1a28287ba2bb1f9c2ea
ms.openlocfilehash: 6739d769c3f7876f67d80554743458b0abd5aae5
ms.contentlocale: is-is
ms.lasthandoff: 02/06/2018

---

# <a name="cost-management-power-bi-content"></a>Kostnaðarstjórnun Power BI efni

[!include[banner](../includes/banner.md)]

> [!Note]
> Þessi efnispakki hefur verið úreltur eins og lýst er í [Power BI efnispakkar gefnir út á PowerBI.com](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/migration-upgrade/deprecated-features#power-bi-content-packs-published-to-powerbicom).


Þetta efnisatriði lýsir því hvað er innifalið í Power BI-efni kostnaðarstjórnunar. 

Microsoft Power BI-efnið **Kostnaðarstjórnun** er ætlað fyrir bókhaldara birgða eða einstaklinga innan fyrirtækiisins sem bera ábyrgð á birgðum. Power BI-efnið **Kostnaðarstjórnun** veitir rekstrarfélagi innsýn í birgðir og birgðir fyrir verk í vinnslu (VÍV) og hvernig kostnaður flæðir í gegn um þær eftir flokki yfir tíma. Upplýsingarnar er einnig hægt að nota sem ítarlega viðbót við fjárhagsskýrslu

## <a name="key-measures"></a>Lykilráðstafanir

+ Upphafsstaða
+ Lokastaða
+ Nettó breyting
+ Nettóbreyting í %
+ Aldursgreining

## <a name="key-performance-indicators"></a>Afkastavísar
+ Birgðahreyfing
+ Birgðanákvæmni

Megingagnaveita fyrir CostAggregatedCostStatementEntryEntity er taflan CostStatementCache. Þessari töflu er stjórnað af ramma skyndiminnis gagnasafns. Sjálfgefið er að taflan sé uppfærð á 24 tíma fresti en hægt er að virkja handvirkar uppfærslur í skilgreiningu gagnaskyndiminnis. Síðan er hægt að gera handvirka uppfærslu á vinnusvæðinu **Kostnaðarstjórnun** eða **Kostnaðargreiningu**. Eftir að uppfærslan á CostStatementCache hefur verið keyrð verður að uppfæra OData-tenging í Power BI.com til að sjá uppfærð gögn á svæði. Frávikin (innkaup, framleiðsla) sem eru mæld í þessu Power Bi-efni snerta aðeins atriði sem eru metin af aðferð Staðalkostnaðar birgðir. Framleiðslufrávik eru reiknuð sem mismunurinn milli virks kostnaðar og innleysts kostnaðar. Framleiðslufrávik er reiknað þegar framleiðslupöntun er með stöðuna **Lokið**. Frekari upplýsingar um gerð framleiðslufrávika og hvernig hver gerð er reiknuð út er að finna í [Um greiningu frávika fyrir lokna framleiðslupöntun](https://technet.microsoft.com/en-us/library/gg242850.aspx).


## <a name="metrics-that-are-included-in-the-power-bi-content"></a>Mælikvarðar sem eru hafðir með í Power BI-efni
Innihaldið inniheldur hóp af skýrslusíðum. Hver síða samanstendur af safni mælikvarða sem eru sýndir sem myndrit, reitir og töflur. Í eftirfarandi töflu er yfirlit yfir myndbirtingar í Power BI-efni **Kostnaðarstjórnun**.

| Skýrslusíða | Gröf | Titlar |
|---|---|---|
|Heildarbirgðir (Sjálfgefið eftir núgildandi tímabili) |Nákvæmni |Birgðamælingar:<br>Lokastaða birgða<br>Nettóbreyting birgða<br>Nettóbreyting birgða %<br>|
| |Birgðahreyfing | |
| |Lokastaða birgða eftir tilfangaflokki | |
| |Nettóbreyting birgða eftir stigi flokksheitis 1 og stigi flokksheitis 2| |
| |Innkaupafrávik eftir tilfangaflokki og stigi flokksheitis 3 | |
|Birgðir eftir svæði (Sjálfgefið eftir núgildandi tímabili) |Lokastaða birgða eftir Heiti seturs og tilfangaflokki | |
| |Birgðahreyfingar eftir Heiti seturs og tilfangaflokki | |
| |Lokastaða birgða eftir borg og tilfangaflokki | |
|Birgðir eftir tilfangaflokki (Sjálfgefið eftir núgildandi tímabili) |Birgðamælingar | |
| |Birgðanákvæmni eftir upphæð eftir tilfangaflokki | |
| |Birgðahreyfingar eftir upphæð eftir tilfangaflokki | |
|Birgðir ár frá ári (Sjálfgefið núgildandi ár gegn fyrra ári) |Birgðamælingar | |
| |Afkastavísar birgða:<br>Birgðahreyfing<br>Birgðanákvæmni | |
| |Lokastaða birgða eftir ári og tilfangaflokki | |
| |Innkaupafrávik eftir ári og stigi flokksheitis 3 | |
|Aldursdreifing birgða (Sjálfgefið eftir núgildandi ári) |Aldursdreifing birgða eftir ársfjórðungi og Tilfangaflokki | |
| |Aldursdreifing birgða eftir ársfjórðungi og svæðaheiti | |
|Heildar VÍV (Sjálfgefið eftir núgildandi tímabili) |Nettóbreyting VÍV eftir stigi flokksheitis 1 og stigi flokksheitis 2 |VÍV-mælingar vinnu í gangi:<br>Lokastaða VÍV<br>Nettóbreyting VÍV<br>Nettóbreyting VÍV %<br> |
| |Framleiðslufrávik eftir tilfangaflokki og stigi flokksheitis 3 | |
| |Nettóbreyting VÍV eftir tilfangaflokki | |
|VÍV eftir svæði (Sjálfgefið eftir núgildandi tímabili) |VÍV-mælingar vinnu í gangi | |
| |Nettóbreyting VÍV eftir svæðaheiti og stigi flokksheitis 2 | |
| |Framleiðslufrávik eftir svæðaheiti og stigi flokksheitis 3 | |

## <a name="understanding-the-data-model-and-entities"></a>Skilja gagnalíkan og einingar
Gögn Finance and Operations eru notuð til að fylla út skýrslusíður í Power BI-efninu **Kostnaðarstjórnun**. Þessi gögn eru birt sem uppsafnaðar mælingar sem stigbundnar eru í einingaversluninni sem Microsoft SQL-gagnagrunnur sem er fínstilltur fyrir greiningu. Frekari upplýsingar eru í [Yfirlit yfir samþættingu Power BI við einingaverslun](power-bi-integration-entity-store.md) Eftirfarandi lykiluppsafnaðar mælingar eru notaðar sem grunnur að efninu.

| Eining            | Lykiluppsafnaðar mælingar | Gagnagjafi fyrir Finance and Operations | Svæði             | lýsing                       |
|-------------------|---------------------------|---------------------------------------------|-------------------|-----------------------------------|
| Færslur yfirlits | Nettó breyting                | CostAggregatedCostStatementEntryEntity      | sum(\[upphæð\])   | Upphæð í bókhaldsgjaldmiðli |
| Færslur yfirlits | Magn nettóbreytingar       | CostAggregatedCostStatementEntryEntity      | sum(\[magn\]) |                                   |

Eftirfarandi tafla sýnir hvernig lykiluppsafnaðar mælingar eru notaðar til að stofna nokkrar útreikningsmælingar í gagnamengi efnisins.

| Mæla                                 | Hvernig mælieining er reiknuð                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|-----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Upphafsstaða                       | \[Lokastaða\]-\[Nettóbreyting\]                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| Magn upphafsstöðu              | \[Magn lokastöðu\]-\[Magn nettóbreytingar\]                                                                                                                                                                                                                                                                                                                                                                                                                        |
| Lokastaða                          | CALCULATE(SUM(\[Upphæð\]), FILTER(ALLEXCEPT(‚Fjárhagsdagatöl', ‚Fjárhagsdagatöl'\[LedgerRecId\], ‚einingar'\[kenni\], ‚einingar'\[Heiti\], 'Fjárhagur'\[Gjaldmiðill\], 'Fjárhagur'\[Lýsing\], 'Fjárhagur'\[Heiti\]), 'Fjárhagsdagatal'\[Date\] &lt;= MAX('Fiscal dagatal'\[Date\])))                                                                                                                                                                                           |
| Magn lokastöðu                 | CALCULATE(SUM(\[Magn\]), FILTER(ALLEXCEPT(‚Fjárhagsdagatöl', ‚Fjárhagsdagatöl'\[LedgerRecId\], ‚einingar'\[kenni\], ‚einingar'\[Heiti\], 'Fjárhagur'\[Gjaldmiðill\], 'Fjárhagur'\[Lýsing\], 'Fjárhagur'\[Heiti\]), 'Fjárhagsdagatal'\[Date\] &lt;= MAX('Fiscal dagatal'\[Date\])))                                                                                                                                                                                         |
| Upphafsstaða birgða             | CALCULATE(\[Upphafsstaða\], 'Færslur yfirlits'\[Yfirlit Gerð\] = "Birgðir")                                                                                                                                                                                                                                                                                                                                                                                      |
| Lokastaða birgða                | CALCULATE(\[Lokastaða\], 'Færslur yfirlits'\[Yfirlit Gerð\] = "Birgðir")                                                                                                                                                                                                                                                                                                                                                                                         |
| Nettóbreyting birgða                    | CALCULATE(\[Nettóbreyting\], 'Færslur yfirlits'\[Yfirlit Gerð\] = "Birgðir")                                                                                                                                                                                                                                                                                                                                                                                             |
| Magn nettóbreytingar birgða           | CALCULATE(\[Magn nettóbreytingar\], 'Færslur yfirlits'\[Yfirlit Gerð\] = "Birgðir")                                                                                                                                                                                                                                                                                                                                                                                    |
| Nettóbreyting birgða %                  | IF(\[Lokastaða birgða\] = 0, 0, \[Nettóbreyting birgða\] / \[Lokastaða birgða\])                                                                                                                                                                                                                                                                                                                                                                           |
| Birgðahreyfingar eftir upphæð                | if(OR(\[Meðaltalsstaða birgða\] &lt;= 0, \[Birgðir seldar eða notað vandamál\] &gt;= 0), 0, ABS(\[Birgðir seldar eða notað vandamál\])/\[Meðaltalsstaða birgða\])                                                                                                                                                                                                                                                                                                  |
| Meðaltalsstaða birgða               | (\[Lokastaða birgða\] + \[Upphafsstaða birgða\]) / 2                                                                                                                                                                                                                                                                                                                                                                                                       |
| Birgðir seldar eða notað vandamál       | \[Birgðir seldar\] + \[Notaður efniskostnaður birgða\]                                                                                                                                                                                                                                                                                                                                                                                                                  |
| Notaður efniskostnaður birgða        | CALCULATE(\[Nettóbreyting birgða\], Færslur yfirlits'\[Flokksheiti - stig 2\_\] = "ConsumedMaterialsCost")                                                                                                                                                                                                                                                                                                                                                            |
| Birgðir seldar                          | CALCULATE(\[Nettóbreyting birgða\], Færslur yfirlits'\[Flokksheiti - stig 2\_\] = „Sold")                                                                                                                                                                                                                                                                                                                                                                             |
| Birgðanákvæmni eftir upphæð            | IF(\[Lokastaða birgða\] &lt;= 0, IF(OR(\[Talin upphæð birgða\] &lt;&gt; 0, \[Lokastaða birgða\] &lt; 0), 0, 1), MAX(0, (\[Lokastaða birgða\] - ABS(\[Talin upphæð birgða\]))/\[Lokastaða birgða\]))                                                                                                                                                                                                                              |
| Talin upphæð birgða                | CALCULATE(\[Nettóbreyting birgða\], Færslur yfirlits'\[Flokksheiti - stig 3\_\] = „Counting")                                                                                                                                                                                                                                                                                                                                                                         |
| Aldursdreifing birgða                         | if(ISBLANK(max(‚Fjárhagsdagatal'\[Dagsetning\])), blank(), MAX(0, MIN(\[Innhreyfingamagn aldursdreifingar birgða\], \[Magn lokastöðu aldursdreifingar birgða\] - \[Innhreyfingamagn aldursdreifingar birgða í framtíðinni\]))) \* \[Meðaleiningarkostnaður birgða\]                                                                                                                                                                                                                                |
| Innhreyfingamagn aldursdreifingar birgða       | IF(\[minDate\] = \[minDateAllSelected\], CALCULATE(\[Magn nettóbreytingar birgða\], 'Færslur yfirlits'\[Magn\] &gt; 0, FILTER(ALLEXCEPT('Fjárhagsdagatöl', 'Fjárhagsdagatöl'\[LedgerRecId\], ‚einingar'\[ID\], ‚einingar'\[Heiti\], 'Fjárhagur'\[Gjaldmiðill\], ‚Fjárhagur'\[Lýsing\], 'Fjárhagur'\[Heiti\]), ‚Fjárhagsdagatöl'\[Dagsetning\] &lt;= MAX(‚Fjárhagsdagatöl'\[Dagsetning\]))), CALCULATE(\[Magn nettóbreytingar birgða\], ‚Færslur yfirlits'\[Magn\] &gt; 0)) |
| Magn lokastöðu aldursdreifingar birgða | \[Magn lokastöðu birgða\] + CALCULATE(\[Magn nettóbreytingar birgða\], FILTER(ALLEXCEPT(‚Fjárhagsdagatöl', 'Fjárhagsdagatöl'\[LedgerRecId\], ‚einingar'\[ID\], ‚einingar'\[Heiti\], 'Fjárhagur'\[Gjaldmiðill\], ‚Fjárhagur'\[Lýsing\], 'Fjárhagur'\[Heiti\]), 'Fjárhagsdagatöl'\[Date\] &gt; max('Fjárhagsdagatöl'\[Date\]) ))                                                                                                                                 |
| Innhreyfingar aldursdreifingar birgða í framtíðinni  | CALCULATE(\[Nettóbreyting birgða\], 'Færslur yfirlits'\[Upphæð\] &gt; 0, FILTER(ALLEXCEPT('Fjárhagsdagatöl', 'Fjárhagsdagatöl'\[LedgerRecId\], ‚einingar'\[ID\], ‚einingar'\[Heiti\], ‚Fjárhagur'\[Gjaldmiðill\], ‚Fjárhagur'\[Lýsing\], ‚Fjárhagur'\[Name\]), 'Fjárhagsdagatöl'\[Date\] &gt; MAX('Fjárhagsdagatöl'\[Date\])))                                                                                                                                             |
| Meðaleiningarkostnaður birgða                 | CALCULATE(\[Lokastaða birgða\] / \[Magn lokastöðu birgða\],ALLEXCEPT('Fjárhagsdagatöl', 'Fjárhagsdagatöl'\[LedgerRecId\], ‚einingar'\[ID\], ‚einingar'\[Name\], ‚Fjárhagur'\[Gjaldmiðill\], ‚Fjárhagur'\[Lýsing\], ‚Fjárhagur'\[Heiti\]))                                                                                                                                                                                                                 |
| Innkaupafrávik                      | CALCULATE(SUM(\[Upphæð\]), 'Færslur yfirlits'\[Flokksheiti - stig 2\_\] = "Keypt", 'Færslur yfirlits'\[Gerð yfirlits\] = „Frávik")                                                                                                                                                                                                                                                                                                                              |
| Upphafsstaða VÍV                   | CALCULATE(\[Upphafsstaða\], 'Færslur yfirlits'\[Gerð yfirlits\] = „VÍV")                                                                                                                                                                                                                                                                                                                                                                                            |
| Lokastaða VÍV                      | CALCULATE(\[Lokastaða\], 'Færslur yfirlits'\[Gerð yfirlits\] = „VÍV")                                                                                                                                                                                                                                                                                                                                                                                               |
| Nettóbreyting VÍV                          | CALCULATE(\[Nettóbreyting\], Færslur yfirlits'\[Gerð yfirlits\] = „VÍV")                                                                                                                                                                                                                                                                                                                                                                                                   |
| Nettóbreyting VÍV %                        | IF(\[Lokastaða VÍV\] = 0, 0, \[Nettóbreyting VÍV\] / \[Lokastaða VÍV\])                                                                                                                                                                                                                                                                                                                                                                                             |
| Framleiðslufrávik                    | CALCULATE(SUM(\[Upphæð\]), 'Færslur yfirlits'\[Flokkaheiti - stig 2\_\] = "ManufacturedCost", 'Statement entries'\[Gerð yfirlits\] = "Variance")                                                                                                                                                                                                                                                                                                                      |
| Flokksheiti - stig 1                 | switch(\[Category name - level 1\_\], "None", "None", "NetSourcing", "Net sourcing", "NetUsage", "Net usage", "NetConversionCost", "Net conversion cost", "NetCostOfGoodsManufactured", "Net cost of goods manufactured", "BeginningBalance", "Beginning balance")                                                                                                                                                                                                         |
| Flokksheiti - stig 2                 | switch(\[Category name - level 2\_\], "None", "None", "Procured", "Procured", "Disposed", "Disposed", "Transferred", "Transferred", "Sold", "Sold", "ConsumedMaterialsCost", "Consumed material cost", "ConsumedManufacturingCost", "Consumed manufacturing cost", "ConsumedOutsourcingCost", "Consumed outsourcing cost", "ConsumedIndirectCost", "Consumed indirect cost", "ManufacturedCost", "Manufactured cost", "Variances", "Variances")                            |
| Flokksheiti - stig 3                 | switch(\[Category name - level 3\_\], "None", "None", "Counting", "None", "ProductionPriceVariance", "Production price", "QuantityVariance", "Quantity", "SubstitutionVariance", "Substitution", "ScrapVariance", "Scrap", "LotSizeVariance", "Lot size", "RevaluationVariance", "Revaluation", "PurchasePriceVariance", "Purchase price", "CostChangeVariance", "Cost change", "RoundingVariance", "Rounding variance")                                                   |

Eftirfarandi lykilvíddir eru notaðar sem síur til að sneiða uppsafnaðar mælingar þannig að hægt sé að veita meiri uppskiptingu og dýpri greiningarinnsýn.

| Eining           | Dæmi um eigindir                       |
|------------------|----------------------------------------------|
| Einingar         | Skilríki, heiti                                     |
| Fjárhagsdagatöl | Almanakm Mánuður, Tímabil, Ársfjórðungur, Ár       |
| Markmið KPI (afkastavísis)        | Markmið birgðanákvæmni, markmið birgðahreyfingar |
| Fjárhagur          | Gjaldmiðill, heiti, lýsing                  |
| Svæði            | Skilríki, heiti, land, borg                      |






