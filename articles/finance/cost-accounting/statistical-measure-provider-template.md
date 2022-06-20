---
title: Sniðmát veitu fyrir meðlimi tölfræðivídda og tölfræðiveita
description: Þessi grein veitir upplýsingar um tölfræðivíddarmeðlimi og sniðmát fyrir tölfræðilega mælikvarðaveitu.
author: AndersGirke
ms.date: 06/16/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CAMCostAccountingLedgerSourceEntryProvider, CAMStatisticalDimension, CAMAXStatisticalMeasureProviderTemplate, CAMAXStatisticalMeasureProviderConfiguration, CAMStatisticalDimensionMember, CAMDataConnectorStatisticalMeasure, CAMImportedStatisticalMeasure, CAMImportedStatisticalMeasureProviderConfiguration
audience: Application User
ms.reviewer: twheeloc
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: twheeloc
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 55f4f1e93eb45530bed886bc46acd1420160eb38
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8904644"
---
# <a name="provider-templates-for-statistical-dimension-members-and-measure-providers"></a>Sniðmát veitu fyrir meðlimi tölfræðivídda og tölfræðiveita

[!include [banner](../includes/banner.md)]

Tölfræðileg vídd og aðildarfélögum eru notaðir til að skrá og stjórna ekki-peningalegt færslur í kostnaðarbókhald. Hægt er að nota meðlimi víddar talnagagna fyrir tvenns konar tilgang:

- Eins og grunnupphæð í reglum eins og úthlutun fyrir dreifingu eða kostnað kostnaðar úthlutun
- Til að tilkynna notkun ekki-gjaldmiðill

## <a name="statistical-dimension"></a>Tölfræðileg vídd

Tölfræðileg vídd hefur einkvæmt heiti og safn meðlimi víddar einkvæmt. Tölfræðilega vídd er úthlutað í kostnaðarbókhaldi fjárhags kenni. Þessi tengsl ties allar samsvarandi tölfræðilega meðlimi víddar í kostnaðarbókhaldi fjárhag. Þar af leiðandi tölfræðilega allar færslur verður stofnuð í samhengi við fjárhag kostnaðarbókhalds.

> [!NOTE]
> Tölfræðileg vídd getur tengst fleiri en einn fjárhagslykil kostnaðarbókhalds.

Hér er dæmi um tölfræðilega vídd.

| Nafn                        | Gagnatengi fyrir víddarstök |
|-----------------------------|--------------------------------------|
| Samnýttu Tölfræðilega einingar | Innflutt víddarstök           |

Hér er dæmi um tölfræðilega vídd sem úthlutað hefur verið í fjárhag í kostnaðarbókhaldi.

| Nafn                  | Bókhaldsgjaldmiðill | Gerð gengis | Fjárhagsdagatal | Vídd kostnaðareiningar | Tölfræðileg vídd       |
|-----------------------|---------------------|--------------------|-----------------|------------------------|-----------------------------|
| Stjórnunarbókhald | USD                 | Föst gjaldmiðli  | Reikningstímabil   | Samnýttu Kostnaðarverð einingar   | Samnýttu Tölfræðilega einingar |

## <a name="statistical-dimension-members"></a>Tölfræðileg víddarstök

Aðili tölfræðilega vídd táknar aðila sem þú vilt ekki-peningalegt mælingar til að skrá. Hægt er að nota þessar mælingar sem grunnur við úthlutun eða rétt í skýrslunni ekki-peningalegt gildi.

Hægt er að stofna meðlimi víddar vinnslu handvirkt. Einnig er þær geta verið fluttur úr skrá með í Gögnum innflutningur/útflutningur stjórnunartæki.

Tölfræðilega vídd aðili verður sjálfkrafa í forskilgreindu úthlutun sem grunnverð. Hægt er að nota sem úthlutun grunneining í reglur eða villulausrar innfærslu í öðrum gerðum af grunnum úthlutun.

Hér eru nokkur dæmi um meðlimi víddar dæmigerðan vinnslu.

| Heiti tölfræðilegrar víddar  | Tölfræðileg einingar | lýsing             | Eining |
|-----------------------------|----------------------|-------------------------|------|
| Samnýttu Tölfræðilega einingar | FTE                  | Starfsmenn í fullu starfi     | Ea.  |
| Samnýttu Tölfræðilega einingar | Rafmagn          | Notkun electricity | kWh  |
| Samnýttu Tölfræðilega einingar | Þjónustupakka CC              | Kostnaðarstaður umbúðir   | Klst. |

## <a name="statistical-measure-provider-template"></a>Veitusniðmát tölfræðiaðgerðar

Talnagögn mælingar geta átt sér margar gerðir aðila. Dynamics 365 Finance er frábær uppspretta til að draga tölfræðilegar mælingar úr. Hægt er að nota sniðmát tölfræðilega mæling þjónustuveita skilgreiningu auðveldlega tölfræðilega mælieiningar sem óskað er eftir að draga.

Skilgreiningar á tölfræðilega mæling þjónustuveita sniðmát er almenna og hægt að margnota lykilorð með mörgum meðlimi víddar vinnslu.

> [!NOTE]
> Hægt er að nota allar töflur sem innihalda fjárhagsvíddir sem uppruninn fyrir talnagögn mælingar.

**Dæmi: Talningar á starfsmenn fyrir hvern kostnaðarstað**

Talning á starfsmenn fyrir hvern kostnaðarstað er tölfræðilega mælieiningar sem nota má í mismunandi tilgangi veita managerial innsýn:

- Í tölfræðilegum skýrslugerð próf með kostnaðarstað
- Úthlutun grundvallar fyrir ýmsan kostnað
- Innri kostnaðarhlutfall með kostnaðarstaður:

    - Kostnaður eftir starfsmönnum
    - Tekjur af starfsmanni

Taflan HcmEmployment geymir lista yfir alla starfsmenn í því tilviki. Þessi tafla er altæka töflu. Þess vegna færslur ekki eru kostnaðarjafnaðar tengjast í ákveðið svæði.

Hér er dæmi um starfsmenn í HcmEmployment.

| Nafn       | Kostnaðarstaður | lýsing   | Gerð starfskrafts |
|------------|-------------|----|-------------|
| Starfsmaður 1 | CC001       | Mannauður | Starfsmaður    |
| Starfsmaður 2 | CC002       | FI | Starfsmaður    |
| Starfsmaður 3 | CC002       | FI | Starfsmaður    |
| Starfsmaður 4 | CC003       | Upplýsingatækni | Starfsmaður    |
| Starfsmaður 5 | CC003       | Upplýsingatækni | Starfsmaður    |
| Starfsmaður 6 | CC002       | FI | Verktaki  |

Þegar stofnuð er **Tölfræðilega mæling þjónustuveita sniðmát** aðsetursbókarfærslu, verður að ákveða hvaða aðgerð á að nota:

- **Talning** – talningu færslna á hvern hlut kostnaðar er flutt.
- **Samtala** – samtala fyrir færslur fyrir hvern hlut kostnaðar er flutt. (Í **Samtölu** svæði og **Dagsetningu** svæði eru nauðsynleg.)

## <a name="using-the-count-function"></a>Með því að nota aðgerðina Teljara

Til dæmis tölfræðilega mæling þjónustuveita sniðmát hægt að setja upp hátt.

| Nafn  | Aðgerð | Frumtafla  | Summusvæði      | Dagsetningarsvæði     |
|-------|----------|---------------|----------------|----------------|
| Starfsmanna í fullu Starfi  | Fjöldi    | HcmEmployment | Ekki tiltækt | Ekki tiltækt |

Einnig er hægt að bæta einum eða fleiri afmarkanir til þess að þrengja mælingar úr töflunni uppruna.

Í þessu dæmi, eigi rétt talningu allra starfsmanna í fullu (starfsmanna í fullu Starfi), er hægt að bæta ýmsum í í **gerð Starfsmanns** svæði. Í í **Skilyrði** valið **Starfsmaður** til að takmarka úttak hátt.

**Afmarkanir**

| Frumtafla  | Svæði       | Skilyrði |
|---------------|-------------|----------|
| HcmEmployment | Gerð starfskrafts | Starfsmaður |

Áður en talnagögn mælinga er hægt að fá í kostnaðarbókhaldi, þarf að koma tengslin á milli tölfræðilega mæling þjónustuveita sniðmátið og stak tölfræðilega vídd. Þessi tengsl eru stofnuð fyrir hverja kostnaðarbókhald fjárhags- og útgáfu. Vensl samanstendur af connector gögn og gögn þjónustuveita. Mögulegt að hafa nokkrar connectors gögn og aðilar gögn fyrir hvern tölfræðilega vídd.

> [!NOTE]
> Í þessu dæmi er mælt verður að stofna aðeins fyrir þá **Raun útgáfu**.

Farið **kostnaðarbókhald fjárhags** \> **Raunútgáfu** \> **Stýra** \> **Talnagögn mælingar** koma á í tengslum við. Fyrir þessa atburðarás skaltu velja **Dynamics 365 Finance – Tölfræðilegar mælingar** gagnatengi, vegna þess að við viljum draga gögn úr Fjármálum.

**Uppruni gagna**

| Nafn        | Gagnatengi                                                                     | Tölfræðilegt víddarstak |
|-------------|------------------------------------------------------------------------------------|------------------------------|
| Starfsmanna í fullu Starfi D365FO | Dynamics 365 Finance – Tölfræðilegar mælingar | Starfsmanna í fullu Starfi                         |

**Skilgreining gagnaveitanda**

| Nafn vinnslu |
|---------------------------|
| Starfsmanna í fullu Starfi                      |

Þegar frumgögnin fyrir vinnslu mæling er keyrð er tölfræðilega eftirfarandi færslur eru stofnaðar í kostnaðarbókhaldi.

**Færslubók**

| Færslubók | Færslubókargerð                       | Fjárhagsdagatalstímabil | Ár   |  Tímabil  |  Útgáfa | Upprunafærslur gagnatengis|
|---------|------------------------------------|------------------------|--------|----------|----------|------------------------------|
| 00001   | Tölfræðileg færsla flutningabókar | Fjárhagur                 | 2017   | 1. tímabil | Fjárhagur CA USMF | Starfsmanna í fullu Starfi                   |

**Tölfræðileg færsla flutningabókafærslna**

| Dagsetning reikningsskila | Mæligildi | Tölfræðileg einingar |   lýsing       | Kostnaðarstaður |
|-----------------|-----------|---------------------|---------------------|-------------|
| 31-01-2017      | 1,00      | Starfsmanna í fullu Starfi                | Starfsmenn í fullu starfi | CC001       |
| 31-01-2017      | 2.00      | Starfsmanna í fullu Starfi                | Starfsmenn í fullu starfi | CC002       |
| 31-01-2017      | 2.00      | Starfsmanna í fullu Starfi                | Starfsmenn í fullu starfi | CC003       |

**Tölfræðilegar færslur**

| Kostnaðarhlutur |  lýsing  | Dagsetning reikningsskila | Tölfræðilegt víddarstak |  lýsing        | Mæligildi |
|-------------|----|-----------------|------------------------------|---------------------|-----------|
| CC001       | Mannauður | 31-01-2017      | Starfsmanna í fullu Starfi                         | Starfsmenn í fullu starfi | 1,00      |
| CC002       | FI | 31-01-2017      | Starfsmanna í fullu Starfi                         | Starfsmenn í fullu starfi | 2.00      |
| CC003       | Upplýsingatækni | 31-01-2017      | Starfsmanna í fullu Starfi                         | Starfsmenn í fullu starfi | 2.00      |

Ef starfsmanna í fullu Starfi fyrirfram vídd stak úthlutunargrunn er úthlutað sem grunnur við úthlutun í regla dreifingu dreift kostnað með því að nota eftirfarandi stuðull úthlutun.

| Kostnaðarhlutur | lýsing    | Mæligildi | Úthlutunarþáttur |
|-------------|----|-----------|-------------------|
| CC001       | Mannauður | 1,00      | (1/5) × upphæð    |
| CC002       | FI | 2.00      | (2/5) × upphæð    |
| CC003       | Upplýsingatækni | 2.00      | (2/5) × upphæð    |

## <a name="using-the-sum-function"></a>Með aðgerðinni Samtöluna

Framleiðsla kostnaðarstað, CC010 (Þyngd), er ábyrgur fyrir þyngd fyrir vörur áður en þær eru sendar til viðskiptavina. Kostnaður beina vinnu er bætt við vörur í gegnum uppskrift (BOM) og leið. Óbeins kostnaðar fyrir keyrslu á kostnaðarstað verður einnig að úthluta framleiddri vöru. Oft, er besta tölfræðilega mælingarinnar fyrir slíkar úthlutun fjöldi skráðra framleiðslutíma fyrir hverja vöru innan tiltekins tímabils.

Taflan ProdRouteTrans geymir alla vinnu framleiðslufærslur eftir lögaðili DataAreadID.

Hér er dæmi um ProdRouteTrans töflu.

| Tilvísun        | Númer | Aðgerð | Gerð | Tími  | Efnisleg dagsetning | Heiti afurðarafbrigðis (Fjárhagsvídd) | Lögaðili |
|------------------|--------|-----------|------|-------|---------------|-------------------------------------|--------------|
| Framleiðslupöntun | P0001  | Pakkning | Tími | 8,00  | 01-01-2017    | Appelsínurauðir juice B2B                    | USMF         |
| Framleiðslupöntun | P0001  | Pakkning | Tími | 8,00  | 02-01-2017    | Appelsínurauðir juice B2B                    | USMF         |
| Framleiðslupöntun | P0002  | Pakkning | Tími | 4,00  | 03-01-2017    | Appelsínurauðir juice Neytanda               | USMF         |
| Framleiðslupöntun | P0003  | Pakkning | Tími | 4,00  | 03-01-2017    | Appelsínurauðir juice Neytanda               | USMF         |
| Framleiðslupöntun | P0004  | Reconst.  | Tími | 10,00 | 03-01-2017    | Appelsínurauðir juice Neytanda               | USMF         |

Þegar stofnuð er **Tölfræðilega mæling þjónustuveita sniðmát** aðsetursbókarfærslu, verður að ákveða hvaða aðgerð á að nota:

- **Talning** – talningu færslna á hvern hlut kostnaðar er flutt.
- **Samtala** – samtala fyrir færslur fyrir hvern hlut kostnaðar er flutt. (Í **Samtölu** svæði og **Dagsetningu** svæði eru nauðsynleg.)

Sniðmátið þjónustuveita tölfræðilega mæling hægt að setja upp hátt.

| Nafn    | Aðgerð | Frumtafla   | Summusvæði | Dagsetningarsvæði    |
|---------|----------|----------------|-----------|---------------|
| Þjónustupakka CC | Samtals      | ProdRouteTrans | Tímar     | Efnisleg dagsetning |

Einnig er hægt að bæta sviðum þrengja mælingar uppruna töflu.

Í þessu dæmi, eigi rétt samtölu tíma sem eru tengdar við vinnustöð CC010 Þyngd kostnaðar er hægt að bæta ýmsum í í **Aðgerð** svæði. Í því **Skilyrði** skal velja **Þyngd** til að takmarka úttak.

**Afmarkanir**

| Frumtafla   | Svæði     | Skilyrði  |
|----------------|-----------|-----------|
| ProdRouteTrans | Aðgerð | Pakkning |

Áður en talnagögn mælinga er hægt að fá í kostnaðarbókhaldi, þarf að koma tengslin á milli tölfræðilega mæling þjónustuveita sniðmátið og stak tölfræðilega vídd. Þessi tengsl eru stofnuð fyrir hverja kostnaðarbókhald fjárhags- og útgáfu. Vensl samanstendur af connector gögn og gögn þjónustuveita. Mögulegt að hafa nokkrar connectors gögn og aðilar gögn fyrir hvern tölfræðilega vídd.

> [!NOTE]
> Í þessu dæmi er mælt verður að stofna aðeins fyrir þá **Raun útgáfu**.

Farið **kostnaðarbókhald fjárhags** \> **Raunútgáfu** \> **Stýra** \> **Talnagögn mælingar** koma á í tengslum við. Fyrir þessa atburðarás skaltu velja **Dynamics 365 Finance – Tölfræðilegar mælingar** gagnatengi, vegna þess að við viljum draga gögn úr Fjármálum.

**Uppruni gagna**

| Nafn           | Gagnatengi                                                                     | Tölfræðilegt víddarstak |
|----------------|------------------------------------------------------------------------------------|------------------------------|
| Pakka CC D365FO | Dynamics 365 Finance – Tölfræðilegar mælingar | Þjónustupakka CC                      |

Kerfið viðurkennir ProdRouteTrans er í töfluna þar sem hver færslan tilheyrir sérstakur lögaðili. Þess vegna er spurt verður að velja lögaðili sem á að flytja inn færslur úr.

**Skilgreining gagnaveitanda**

| Nafn vinnslu | Lögaðili |
|---------------------------|--------------|
| Þjónustupakka CC                   | USMF         |

Eftir frumgögnin fyrir vinnslu mæling er að vinna eftirfarandi tölfræðilega færslur eru stofnaðar í kostnaðarbókhaldi.

**Færslubók**

| Færslubók | Færslubókargerð                     | Fjárhagsdagatalstímabil | Ár   | Tímabil | Útgáfa   |   Upprunafærslur gagnatengis  |
|---------|----------------------------------|------------------------|--------|---------|----------------|---------|
| 00002   | Tölfræðileg færsla flutningabókar | Fjárhagur               | 2017    | 1. tímabil  | Fjárhagur CA USMF | Þjónustupakka CC |

**Tölfræðileg færsla flutningabókafærslna**

| Dagsetning reikningsskila | Mæligildi | Tölfræðileg einingar |  lýsing          | Afurðarflokkur         |
|-----------------|-----------|---------------------|-----------------------|-----------------------|
| 31-01-2017      | 16,00     | Þjónustupakka CC             | Kostnaðarstaður umbúðir | Appelsínurauðir juice B2B      |
| 31-01-2017      | 8,00      | Þjónustupakka CC             | Kostnaðarstaður umbúðir | Appelsínurauðir juice Neytanda |

**Tölfræðilegar færslur**

| Kostnaðarhlutur           | Dagsetning reikningsskila | Tölfræðilegt víddarstak |    lýsing        | Mæligildi |
|-----------------------|-----------------|------------------------------|-----------------------|-----------|
| Appelsínurauðir juice B2B      | 31-01-2017      | Þjónustupakka CC                      | Kostnaðarstaður umbúðir | 16,00     |
| Appelsínurauðir juice Neytanda | 31-01-2017      | Þjónustupakka CC                      | Kostnaðarstaður umbúðir | 8,00      |

Ef Þjónustupakka CC fyrirfram vídd stak úthlutunargrunn er úthlutað sem grunnur við úthlutun í regla dreifingu kostnaður símtalalistamarkanna með því að nota eftirfarandi stuðull úthlutun.

| Kostnaðarhlutur           | Mæligildi | Úthlutunarþáttur  |
|-----------------------|-----------|--------------------|
| Appelsínurauðir juice B2B      | 16,00     | (16 ÷ 24) × upphæð |
| Appelsínurauðir juice Neytanda | 8,00      | (8 ÷ 24) × upphæð  |

## <a name="imported-statistical-measures"></a>Innfluttar tölfræðiaðgerðir

Hægt er að flytja talnagögn mælingar í kostnaðarbókhaldi með í Gögnum innflutningur/útflutningur stjórnunartæki.

Gögn einingar sem notaðar eru fyrir innflutning kallaður Imported talnagögn mælingar.

> [!NOTE]
> Þessi gögn einingar er sérstaklega hannað til að leyfa að hámarki fimm einkvæmu víddargildum fyrir hverja færslu.

Notkun rafmagns er skráð í Microsoft Excel með því að nota fyrirfram skilgreint snið gagnaeiningarinnar. Eftirfarandi er dæmi.

| Dagsetning reikningsskila | Víddarstak, heiti 1 | Víddarstak, heiti 2 | Víddarstak, heiti 5 | Mæligildi  | Kenni uppruna |
|-----------------|------------------------|------------------------|------------------------|------------|-------------------|
| 31-01-2017      | CC001                  |                        |                        | 2,450.00   | Rafmagn       |
| 31-01-2017      | CC002                  |                        |                        | 4,100.00   | Rafmagn       |
| 31-01-2017      | CC003                  |                        |                        | 15,000.00  | Rafmagn       |

Þegar verið er að flytja gögnin í gegnum gagnastjórnun, gögnin vistuð í kostnaðarbókhaldi stigaðgerðir töflu. Þar af leiðandi er hægt að nota innfluttum gögnum í mörgum fjárhagir kostnaðarbókhalds. Sækja gögn isn't nauðsynleg.

Til að flytja inn gögnin, er farið **gögn flutt Inn** \> **Gögn einingar** \> **Innfluttar talnagögn mælingar**.

| Kenni uppruna | Dagsetning reikningsskila | Mæligildi  | Víddarstak, heiti 1 | Víddarstak, heiti 2 | Víddarstak, heiti 5 |
|-------------------|-----------------|------------|------------------------|------------------------|------------------------|
| Rafmagn       | 31-01-2017      | 2,450.00   | CC001                  |                        |                        |
| Rafmagn       | 31-01-2017      | 4,100.00   | CC002                  |                        |                        |
| Rafmagn       | 31-01-2017      | 15,000.00  | CC003                  |                        |                        |

Áður en talnagögn mælinga er hægt að fá í kostnaðarbókhaldi, þarf að koma tengslin á milli kenni uppruna og stak tölfræðilega vídd. Þessi tengsl eru stofnuð fyrir hverja kostnaðarbókhald fjárhags- og útgáfu. Vensl samanstendur af connector gögn og gögn þjónustuveita. Mögulegt að hafa nokkrar connectors gögn og aðilar gögn fyrir hvern tölfræðilega vídd.

> [!NOTE]
> Í þessu dæmi er mælt verður að stofna aðeins fyrir þá **Raun útgáfu**.

Farið **kostnaðarbókhald fjárhags** \> **Raunútgáfu** \> **Stýra** \> **Talnagögn mælingar** koma á í tengslum við. Þessu dæmi þarf að velja á **Innfluttar talnagögn mælingar** connector gögn, vegna þess að gögn hafi verið flutt inn úr kerfi þriðja aðila í kostnaðarbókhald gegnum Excel.

**Uppruni gagna**

| Nafn        | Gagnatengi                | Tölfræðilegt víddarstak |
|-------------|-------------------------------|------------------------------|
| Rafmagn | Innfluttar tölfræðiaðgerðir | Rafmagn                  |

**Skilgreining gagnaveitanda**

| Kennimerki uppruna innflutnings | Aðgerð | Vídd1   | Vídd2 | Vídd5 |
|--------------------------|----------|--------------|------------|------------|
| Rafmagn              | Samtals      | Kostnaðarstaðir |            |            |

> [!NOTE]
> Þegar afbrigðið þjónustuveita gögn er skilgreind þarf að tilgreina sem hlutur víddir til að bera saman við innfluttar færslur. Þegar frumgögnin fyrir vinnslu mæling er keyrð er tölfræðilega eftirfarandi færslur eru stofnaðar í kostnaðarbókhaldi.

**Færslubók**

| Færslubók | Færslubókargerð                       | Fjárhagsdagatalstímabil | Ár  | Perid  |Útgáfa      |Upprunafærslur gagnatengis |
|---------|------------------------------------|------------------------|-------|--------|---------------|-------------|
| 00002   | Tölfræðileg færsla flutningabókar | Fjárhagur                 | 2017  | 1. tímabil | Fjárhagur CA USMF | Rafmagn |

**Tölfræðileg færsla flutningabókafærslna**

| Dagsetning reikningsskila | Mæligildi  | Kostnaðareining |   lýsing           | Kostnaðarstaður |
|-----------------|------------|--------------|-------------------------|-------------|
| 31-01-2017      | 2,450.00   | Rafmagn  | Notkun electricity | CC001       |
| 31-01-2017      | 4,100.00   | Rafmagn  | Notkun electricity | CC002       |
| 31-01-2017      | 15,000.00  | Rafmagn  | Rafmagnsnotkun | CC003       |

**Tölfræðilegar færslur**

| Kostnaðarhlutur | lýsing | Dagsetning reikningsskila | Tölfræðilegt víddarstak |      lýsing                   | Mæligildi  |
|-------------|----|-----------------|------------------------------|-------------------------|------------|
| CC001       | Mannauður | 31-01-2017      | Rafmagn                  | Notkun electricity | 2,450.00   |
| CC002       | FI | 31-01-2017      | Rafmagn                  | Notkun electricity | 4,100.00   |
| CC003       | Upplýsingatækni | 31-01-2017      | Rafmagn                  | Notkun electricity | 15,000.00  |

Ef Electricity fyrirfram vídd stak úthlutunargrunn er úthlutað sem grunnur við úthlutun í regla dreifingu kostnaður símtalalistamarkanna með því að nota eftirfarandi stuðull úthlutun.

| Kostnaðarhlutur | lýsing   | Mæligildi | Úthlutunarþáttur          |
|-------------|---------------|-----------|----------------------------|
| CC001       | Mannauður            | 2,450.00  | (2.450 ÷ 21.550) × upphæð  |
| CC002       | FI            | 4,100.00  | (4.100 ÷ 21.550) × upphæð  |
| CC003       | Upplýsingatækni            | 15,000.00 | (15.000 ÷ 21.550) × upphæð |

## <a name="additional-resources"></a>Frekari upplýsingar

[Úthlutunargrunnar](allocation-bases.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
