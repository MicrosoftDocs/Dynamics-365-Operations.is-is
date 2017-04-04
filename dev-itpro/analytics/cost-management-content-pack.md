---
title: "Kostnaðarstjórnun Power BI-efni"
description: "Þetta efnisatriði lýsir því hvað er innifalin í stjórnun Kostnaðar Power BI efni. Það útskýrt hvernig á að ná í skýrslur Power BI og veitir upplýsingar um gagnalíkan og einingar sem notaðar eru til að byggja efni."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: AX 7.0.0, Operations
ms.custom: 270314
ms.assetid: 9680d977-43c8-47a7-966d-2280ba21402a
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 388b6398488e6f316c1ec07a00182e81c1dc8d08
ms.openlocfilehash: e4de011e6eeac58643b828b65e24b874d981d5e7
ms.lasthandoff: 03/31/2017


---

# <a name="cost-management-power-bi-content"></a>Kostnaðarstjórnun Power BI-efni

Þetta efnisatriði lýsir því hvað er innifalin í stjórnun Kostnaðar Power BI efni. Það útskýrt hvernig á að ná í skýrslur Power BI og veitir upplýsingar um gagnalíkan og einingar sem notaðar eru til að byggja efni.

# <a name="overview"></a>Yfirlit

Í **stjórnun Kostnaðar** Microsoft Power BI efni er ætluð fyrir birgðir bókarar eða einstaklinga innan fyrirtækisins sem er ábyrgur fyrir birgðir. Í **stjórnun Kostnaðar** Power BI efni veitir heimildir insight í birgðir og birgðir verk í vinnslu (VÍV) og hvernig kostnaður streymir í gegnum þær eftir tegund yfir tíma. Einnig er hægt að nota upplýsingarnar sem nákvæmar viðauki fjárhagsskýrslu.

## <a name="key-measures"></a>Lykill mælir

+ Upphafsstaða
+ Lokastaða
+ Nettó breyting
+ Nettó breyting í %
+ Aldursgreining

## <a name="key-performance-indicators"></a>Afkastavísar
+ Birgðahreyfing
+ Birgðanákvæmni

Aðal gagnagjafa fyrir CostAggregatedCostStatementEntryEntity er CostStatementCache töfluna. Þessi tafla er stjórnað af ramma gagnasafn skyndiminni. Taflan er uppfærður sólarhring en er hægt að virkja handvirkar uppfærslur í skyndiminni skilgreiningu gögn sjálfgefnu. Síðan er hægt að gera handvirkar uppfærslu á **stjórnun Kostnaðar** eða **Greining** vinnusvæði. Eftir uppfærslu CostStatementCache er keyrð, verður að uppfæra tengingu OData Power BI.com til að sjá uppfærð gögn á svæði. Mælingar frávikið (innkaup, framleiðsla) í þessu innihaldi Power BI eiga aðeins við vörur sem eru valuated greiðsluhættinum staðalkostnaðar birgða. Frávik í framleiðslu er reiknað sem mismunur virkan kostnað og raunverulegan kostnað. Framleiðsla frávikið er reiknað út þegar framleiðslupöntunin hefur stöðuna **Lokið**. Nánari upplýsingar um gerðir frávika í framleiðslu og hvernig hverja gerð er reiknuð í [Um greining frávika fyrir framleiðslupöntun sem lokið](https://technet.microsoft.com/en-us/library/gg242850.aspx).

## <a name="accessing-the-power-bi-content"></a>Fara í hugbúnaðarhlutartréð innihald Power BI
Í **stjórnun Kostnaðar** Power BI efni er tiltækt frá PowerBI.com. Nánari upplýsingar um hvernig á að tengjast og sækja skal Microsoft Dynamics 365 fyrir Aðgerðir í [Aðgang Power BI efni úr PowerBI.com](power-bi-home-page.md).

## <a name="metrics-that-are-included-in-the-power-bi-content"></a>Einingar sem eru hafðar með í efni Power BI
Innihald inniheldur safn af skýrslusíðum. Hverri síðu samanstendur af safni einingar sem eru visualized sem gröf reitir og töflur. Eftirfarandi tafla veitir yfirlit yfir sjóngervingum í á **stjórnun Kostnaðar** Power BI efni.

| Skýrslan síðu | Gröf | Titlar |
|---|---|---|
|Almenna birgða (Sjálfgefið gildandi tímabil) |Nákvæmni |Mælingar birgða:<br>Lokastaða birgða<br>Nettó breyting birgða<br>Nettó breyting % birgða<br>|
| |Birgðahreyfing | |
| |Lokastaðan eftir tilfangaflokkur birgða | |
| |Nettó breyting birgða eftir Tegund heiti stig 1 og stig heiti 2| |
| |Innkaupafrávik tilfangaflokkinn og stig heiti 3 | |
|Birgðir eftir svæði (Sjálfgefið gildandi tímabil) |Lokastaðan eftir svæðisheiti og tilfangaflokkur birgða | |
| |Birgðahreyfing eftir svæðisheiti og tilfangaflokk | |
| |Lokastaðan eftir Borg og Tilfanga birgða | |
|Birgðir eftir tilfangaflokkur (Sjálfgefið gildandi tímabil) |Birgðir mælingar | |
| |Birgðanákvæmni eftir upphæð með tilfangaflokk | |
| |Birgðahreyfing af upphæð með tilfangaflokk | |
|Birgðir sölu milli ÁRA (Sjálfgefið gildandi ár samanb. v. fyrra árs) |Birgðir mælingar | |
| |Afkastavísar birgða:<br>Birgðahreyfing<br>Birgðanákvæmni | |
| |Lokastaðan eftir Ári og Tilfanga birgða | |
| |Innkaupafrávik Árs- og heiti stigi 3 | |
|Aldursdreifing birgða (Sjálfgefin með þetta ár) |Aldursdreifing birgða eftir Fjórðungi og Tilfanga | |
| |Aldursdreifing birgða eftir Fjórðungi og Svæði | |
|Almenna VÍV (Sjálfgefið gildandi tímabil) |Nettó VÍV breyta með því að stig heiti 1 og stig heiti 2 |VÍV mælieiningar vinnu í vinnslu:<br>Lokastaða VÍV<br>Nettó breyting VÍV<br>VÍV nettó breyting í %<br> |
| |Framleiðslufrávik eftir tilfangaflokkinn og Tegund 3. stigs heiti | |
| |Nettó breyting VÍV með tilfangaflokk | |
|VÍV eftir svæði (Sjálfgefið gildandi tímabil) |Mælingar samantektarstöðu VÍV | |
| |Nettó VÍV breyta svæðisheiti og stig heiti 2 | |
| |Framleiðslufrávik eftir svæðisheiti og Tegund 3. stigs heiti | |

## <a name="understanding-the-data-model-and-entities"></a>Skilja gagnalíkan og einingar
Dynamics 365 fyrir Aðgerðir sem er notuð til að fylla út skýrslusíðum í á **stjórnun Kostnaðar** Power BI efni. Þessum gögnum er birtur sem uppsöfnuðum mælingum sem stig eru í versluninni Einingar sem er Microsoft SQL-gagnagrunnur sem er fínstillt fyrir greiningu. Nánari upplýsingar, sjá [Yfirlit Power BI samþættingu við verslun Einingar](power-bi-integration-entity-store.md). Eftirfarandi lykli uppsafnaðar mælingar eru notaðar sem grunnur fyrir efni.

| Eining            | Lykill uppsafnaða mælingu | Gagnagjafi fyrir Dynamics 365 fyrir Aðgerðir | Svæði             | lýsing                       |
|-------------------|---------------------------|---------------------------------------------|-------------------|-----------------------------------|
| Uppgjör-færslur | Nettó breyting                | CostAggregatedCostStatementEntryEntity      | Samtala (\[Upphæð\])   | Upphæð í bókhaldsgjaldmiðli |
| Uppgjör-færslur | Nettó breyting magn       | CostAggregatedCostStatementEntryEntity      | Samtala (\[Magn\]) |                                   |

Eftirfarandi tafla sýnir hvernig uppsafnaðar mælingar lykli eru notaðar til að stofna reiknaðar mælieiningar í gagnasafni sem efni.

| Mæla                                 | Hvernig mælieiningu sem er reiknað                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|-----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Upphafsstaða                       | \[Lokastaða\]-\[Nettó breyting\]                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| Upphaf magnstaða              | \[Staða lokamagn\]-\[Nettó breyta magni\]                                                                                                                                                                                                                                                                                                                                                                                                                        |
| Lokastaða                          | REIKNA (SAMTALA (\[Upphæð\]), SÍU (ALLEXCEPT ('Fjárhagsdagatöl', 'Fjárhagsdagatöl'\[LedgerRecId\], 'einingar'\[Kenni\], 'einingar'\[Heiti\], 'Fjárhag'\[Gjaldmiðli\], 'Fjárhag'\[Lýsing\], 'Fjárhag'\[Heiti\]), 'Fjárhagsdagatöl'\[Dagsetning\]&lt;= MAX ('Fjárhagsdagatöl'\[Dagsetning\])))                                                                                                                                                                                           |
| Magnstaða lýkur                 | REIKNA (SAMTALA (\[Magn\]), SÍU (ALLEXCEPT ('Fjárhagsdagatöl', 'Fjárhagsdagatöl'\[LedgerRecId\], 'einingar'\[Kenni\], 'einingar'\[Heiti\], 'Fjárhag'\[Gjaldmiðli\], 'Fjárhag'\[Lýsing\], 'Fjárhag'\[Heiti\]), 'Fjárhagsdagatöl'\[Dagsetning\]&lt;= MAX ('Fjárhagsdagatöl'\[Dagsetning\])))                                                                                                                                                                                         |
| Upphafsstaða birgða             | REIKNA (\[Upphafsstaða\], 'Færslum Uppgjör'\[Yfirlitsgerðin\] = "Birgðir")                                                                                                                                                                                                                                                                                                                                                                                      |
| Lokastaða birgða                | REIKNA (\[Lokastaða\], 'Færslum Uppgjör'\[Yfirlitsgerðin\] = "Birgðir")                                                                                                                                                                                                                                                                                                                                                                                         |
| Nettó breyting birgða                    | REIKNA (\[Nettó breyting\], 'Færslum Uppgjör'\[yfirlitsgerðin\] = "Birgðir")                                                                                                                                                                                                                                                                                                                                                                                             |
| Nettó breyting birgðamagn           | REIKNA (\[Nettó breyta magni\], 'Færslum Uppgjör'\[yfirlitsgerðin\] = "Birgðir")                                                                                                                                                                                                                                                                                                                                                                                    |
| Nettó breyting % birgða                  | EF (\[Birgða lokastaðan\] = 0, 0 \[Birgða nettóbreyting\] / \[Birgða lokastaðan\])                                                                                                                                                                                                                                                                                                                                                                           |
| Birgðahreyfing eftir upphæð                | Ef (OR (\[Birgða meðaltal stöðu\]&lt;= 0 \[Birgðir hafa verið seldar eða notaðar úthreyfingar\]&gt;= 0), 0, ABS (\[Birgðir hafa verið seldar eða notaðar úthreyfingar\]) /\[Birgða meðaltal stöðu\])                                                                                                                                                                                                                                                                                                  |
| Meðaltal birgðastöðu               | (\[Birgða lokastaðan\] + \[Birgða upphafsstöðu\]) / 2                                                                                                                                                                                                                                                                                                                                                                                                       |
| Birgðir hafa verið seldar eða notaðar úthreyfingar       | \[Seldra birgða\] + \[Birgðir notkun efnis kostnaðar\]                                                                                                                                                                                                                                                                                                                                                                                                                  |
| Birgðir eru notaðar efni kostnaðar        | REIKNA (\[Birgða nettóbreyting\], 'Færslum Uppgjör'\[heiti Tegundar - stig 2\_\] = "ConsumedMaterialsCost")                                                                                                                                                                                                                                                                                                                                                            |
| Seldra birgða                          | REIKNA (\[Birgða nettóbreyting\], 'Færslum Uppgjör'\[heiti Tegundar - stig 2\_\] = "Selt")                                                                                                                                                                                                                                                                                                                                                                             |
| Birgðanákvæmni eftir upphæð            | EF (\[Birgða lokastaða\]&lt;= 0, EF (EÐA (\[Birgðir talin upphæð\]&lt;&gt; 0, \[Birgða lokastaða\]&lt; 0), 0, 1), HÁMARKS (0 (\[Birgða lokastaða\] -ABS (\[Birgðir talin upphæð\])) /\[Birgða lokastaða\]))                                                                                                                                                                                                                              |
| Talin upphæð birgða                | REIKNA (\[Birgða nettóbreyting\], 'Færslum Uppgjör'\[heiti Tegundar - 3. stigs\_\] = "Talning")                                                                                                                                                                                                                                                                                                                                                                         |
| Aldursdreifing birgða                         | Ef (ISBLANK (hámarks ('Fjárhagsdagatöl'\[Dagsetning\])), blank(), MAX (0, Lágmark (\[aldursdreifing Birgða innhreyfingar magn\], \[Birgða aldurstímabils lokadagsetningu magnstaða\] - \[aldursdreifing Birgða innhreyfingar magn í framtíðinni\]))) \*\[einingarkostnað avg Birgða\]                                                                                                                                                                                                                                |
| Aldursgreining magn innhreyfingar birgða       | EF (\[minDate\] = \[minDateAllSelected\], REIKNA (\[Birgðamagnið nettó breyting\], 'Færslum Uppgjör'\[Magn\]&gt; 0, SÍU (ALLEXCEPT ('Fjárhagsdagatöl', 'Fjárhagsdagatöl'\[LedgerRecId\], 'einingar'\[Kenni\], 'einingar'\[Heiti\], 'Fjárhag'\[Gjaldmiðli\], 'Fjárhag'\[Lýsingu\], 'Fjárhag'\[Heiti\]), 'Fjárhagsdagatöl'\[Dagsetning\]&lt;= MAX ('Fjárhagsdagatöl'\[Dagsetning\]))), REIKNA (\[Birgðamagnið nettó breyting\], 'Færslum Uppgjör'\[Magn\]&gt; 0)) |
| Staða lokamagn aldursdreifing birgða | \[Lokamagn stöðu birgða\] + REIKNA (\[Birgðamagnið nettóbreyting\], SÍU (ALLEXCEPT ('Fjárhagsdagatöl', 'Fjárhagsdagatöl'\[LedgerRecId\], 'einingar'\[Kenni\], 'einingar'\[Heiti\], 'Fjárhag'\[Gjaldmiðli\], 'Fjárhag'\[Lýsingu\], 'Fjárhag'\[Heiti\]), 'Fjárhagsdagatöl'\[Dagsetning\]&gt; hámarksstig ('Fjárhagsdagatöl'\[Dagsetning\])))                                                                                                                                 |
| Aldurstímabil birgðamóttöku í framtíðinni  | REIKNA (\[Birgða nettó breyting\], 'Færslum Uppgjör'\[Upphæð\]&gt; 0, SÍU (ALLEXCEPT ('Fjárhagsdagatöl', 'Fjárhagsdagatöl'\[LedgerRecId\], 'einingar'\[Kenni\], 'einingar'\[Heiti\], 'Fjárhag'\[Gjaldmiðli\], 'Fjárhag'\[Lýsingu\], 'Fjárhag'\[Heiti\]), 'Fjárhagsdagatöl'\[Dagsetning\]&gt; MAX ('Fjárhagsdagatöl'\[Dagsetning\])))                                                                                                                                             |
| Einingarkostnaður avg birgða                 | REIKNA (\[Birgða lokastaða\] / \[Birgðamagnið lokadagsetning stöðu\], ALLEXCEPT ('Fjárhagsdagatöl', 'Fjárhagsdagatöl'\[LedgerRecId\], 'einingar'\[Kenni\], 'einingar'\[Heiti\], 'Fjárhag'\[Gjaldmiðli\], 'Fjárhag'\[Lýsing\], 'Fjárhag'\[Heiti\]))                                                                                                                                                                                                                 |
| Innkaupafrávik                      | REIKNA (SAMTALA (\[Upphæð\]), 'Færslum Uppgjör'\[heiti Tegundar - stig 2\_\] = "Procured", 'Uppgjör færslum'\[yfirlitsgerðin\] = "Frávik")                                                                                                                                                                                                                                                                                                                              |
| VÍV upphafsstöðu                   | REIKNA (\[Upphafsstaða\], 'Færslum Uppgjör'\[Yfirlitsgerðin\] = "VÍV")                                                                                                                                                                                                                                                                                                                                                                                            |
| Lokastaða VÍV                      | REIKNA (\[Lokastaða\], 'Færslum Uppgjör'\[Yfirlitsgerðin\] = "VÍV")                                                                                                                                                                                                                                                                                                                                                                                               |
| Nettó breyting VÍV                          | REIKNA (\[Nettó breyting\], 'Færslum Uppgjör'\[yfirlitsgerðin\] = "VÍV")                                                                                                                                                                                                                                                                                                                                                                                                   |
| VÍV nettó breyting í %                        | EF (\[VÍV lokastaða\] = 0, 0, \[nettóbreyting VÍV\] / \[VÍV lokastaða\])                                                                                                                                                                                                                                                                                                                                                                                             |
| Frávik í framleiðslu                    | REIKNA (SAMTALA (\[Upphæð\]), 'Færslum Uppgjör'\[heiti Tegundar - stig 2\_\] = "ManufacturedCost", 'Uppgjör færslum'\[yfirlitsgerðin\] = "Frávik")                                                                                                                                                                                                                                                                                                                      |
| Heiti tegundar - stig 1                 | Skipta (\[heiti Tegundar - stig 1\_\], "Ekkert", "Ekkert", "NetSourcing", "Nettó uppruni", "NetUsage", "Nettónotkun", "NetConversionCost", "Nettó umreikningi staðalkostnaðar", "NetCostOfGoodsManufactured", "Nettó kostnaður framleiddra vara", "BeginningBalance", "Upphafsstaða")                                                                                                                                                                                                         |
| Heiti tegundar - stig 2                 | Skipta (\[heiti Tegundar - stig 2\_\], "Ekkert", "Ekkert", "Procured", "Procured", "Disposed", "Disposed", "Transferred", "Transferred", "Selt", "Selt", "ConsumedMaterialsCost" "Notað efnis", "ConsumedManufacturingCost", "Notaða framleiðslu kostnaðar", "ConsumedOutsourcingCost", "Notaða útvistun kostnaður", "ConsumedIndirectCost", "Notað óbeins kostnaðar", "ManufacturedCost", "Manufactured kostnaður", "Frávik", "Frávik")                            |
| Heiti tegundar - stigi 3                 | Skipta (\[heiti Tegundar - 3. stigs\_\], "Ekkert", "Ekkert", "Talning", "Ekkert", "ProductionPriceVariance", "Framleiðsluverð", "QuantityVariance", "Magn", "SubstitutionVariance", "Gildaskiptaeiningar", "ScrapVariance", "Rýrnun", "LotSizeVariance", "Lotustærð", "RevaluationVariance", "Endurmat á", "PurchasePriceVariance", "Innkaupaverð", "CostChangeVariance," "Kostnaðarbreyting", "RoundingVariance", "Sléttunarfrávik")                                                   |

Eftirfarandi lykill eru notaðar þær víddir sem síur til að sneiða uppsafnaðar mælingar til að ná uppskiptingin hærri og veita hærra insights greiningar.

| Eining           | Dæmi um eigindir                       |
|------------------|----------------------------------------------|
| Einingar         | Kenni, Heiti                                     |
| Fjárhagsdagatöl | Dagatal, Mánuður, Tímabil, Fjórðungur, Ár       |
| Markmið KPI (afkastavísis)        | Birgðahreyfing birgðir nákvæmni markmið markmiðs |
| Fjárhagur          | Gjaldmiðill, Heiti, Lýsing                  |
| Svæði            | Kenni, Nafn, Land, Borg                      |

## <a name="additional-resources"></a>Frekari upplýsingar
Hér eru gagnlegir tenglar sem tengjast einingar og að búa til Power BI-efni:

-   [Gagnaeiningar](..\data-entities\data-entities.md)
-   [Stofnun efnispakka fyrirtækis ](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   [Gera gagnalíkön með því að nota Power BI](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [Bæta Power BI-reitum við vinnusvæði](configure-power-bi-integration.md)



