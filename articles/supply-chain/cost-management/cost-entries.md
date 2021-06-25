---
title: Kostnaðarfærslur
description: Þessi grein veitir upplýsingar um kostnaðarfærslur og þegar þær eru stofnaðir. Kostnaðarfærslu er færsla sem skráir magni og kostnað á tilteknu tilviki.
author: AndersGirke
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventCostOnhandItem
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19131
ms.assetid: dd2663d8-bcc0-47b1-b36d-57433143487c
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7b258e111139f52f5ccf3ea3f385a1367576eacd
ms.sourcegitcommit: ff09736563d3cd2bc74c7664edd1767b218401cb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/04/2021
ms.locfileid: "6188537"
---
# <a name="cost-entries"></a>Kostnaðarfærslur

[!include [banner](../includes/banner.md)]

Þessi grein veitir upplýsingar um kostnaðarfærslur og þegar þær eru stofnaðir. Kostnaðarfærslu er færsla sem skráir magni og kostnað á tilteknu tilviki.

Kostnaðarfærslur eru uppsöfnun birgðafærslna sem eru skráðar á virkar fjárhagslegar birgðavíddir.

## <a name="examples"></a>Dæmi
### <a name="example-1-no-cost-entries-are-created"></a>Dæmi 1: Engin kostnaðarfærslur eru stofnaðar

Tilvik flutnings færslubókar er skráð. Tilvikið flytur eitt stykki af vöru A frá staðsetningu A til staðsetningar B. birgðavídd Staðsetningar er ekki talin hluti af kostnaðarhlut. Þess vegna stofnar tilvikið engar kostnaðarfærslur og tvær birgðafærslur.

### <a name="example-2-cost-entries-are-created"></a>Dæmi 2: kostnaðarfærslur eru stofnaðar

Tilvik flutnings færslubókar er skráð. Tilvikið flytur eitt stykki af vöru A frá staðsetningu 1 til staðsetningar 2. Birgðavídd Staðsetningar er talin hluti af hluti af kostnaðarhlut. Þess vegna stofnar tilvikið tvær kostnaðarfærslur og tvær birgðafærslur.

### <a name="example-3-one-cost-entry-is-created"></a>Dæmi 3: ein kostnaðarfærsla er stofnaðar

Tilvik innhreyfingarskjals afurðar er skráð fyrir innkaupapöntun. Tilvikið skráir 100 stykki af vöru A á einingarkostnaði uppá 10,00 bandarískum dollurum (USD). Þar sem vöru A notar raðnúmer til að rekja málefni birgðastjórnunar, er stofnað einkvæmt raðnúmer fyrir hverja vöru sem er móttekin. Þess vegna stofnar tilvikið 100 birgðafærslur og eina kostnaðarfærslu.

## <a name="cost-entries-page"></a>Kostnaðarfærslusíður
Nýja **Kostnaðarfærslu** síðu gerir kleift að skoða og stýra skráningar á kostnaði og magni. Þessi síða er viðbót við **Birgðafærslu** og **Birgðajöfnunar** síður. Færslur eru skráðar í tímaröð fyrir tilvik. Þess vegna er hægt að finna og stjórna uppsafnaðan kostnað á skjótan hátt fyrir ákveðinn viðburð eða öll atvik sem eru tengdar við skjal. Eftirfarandi er dæmi:

-   Tilvik innhreyfingarskjals afurðar er skráð fyrir vöru A. Hundrað stykki eru mótteknar með einingarkostnað 10,00 usd.
-   Nokkrar dögum eftir að reikningstilvikið er skráð, eykst kostnaður í USD 11.00. Þess vegna er heildarupphæðin 1.100. Önnur fylgiskjal er stofnuð til að útskýra mismuninn uppá 100 usd.
-   Nokkrar dögum síðar er óflokkað gjald upp á USD 15.00 til að ná yfir flutningskostnað er skráður á innkaupapöntuninni.

| Fylgiskjal | Dagsetning       | Tilvísun      | Númer | Lotukenni  | Magn | Upphæð  |
|---------|------------|----------------|--------|---------|---------------|----|
| 00001   | 01/01/2015 | Innkaupapöntun | 100001 | 0000101 | 100,00   | 1000,00 |
| 00002   | 20/01/2015 | Innkaupapöntun | 100001 | 0000101 |          | 100,00  |
| 00003   | 31-01-2015 | Leiðrétting     | 100001 | 0000101 |          | 15:00   |

**Kostnaðarfærslur** síðu gerir kleift að sía eftir Skjalakenni og dagsetningu skjals. 

> [!NOTE]
> Kostnaðarfærslur eru aðeins tiltækar fyrir [kostnaðarhluti](cost-object.md) eða útgefnar afurðir.

## <a name="additional-resources"></a>Frekari upplýsingar

[Kostnaðarhlutir](cost-object.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]